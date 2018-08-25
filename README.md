# learning
Repositorio de estudos sobre técnicas de programação. / Repository studies on programming techniques.
public enum MarketType
    {
        Spot,
        Future,
        OptionsSpot,
        OptionsFuture,
        Forward,
        EtfPrimaryMarket,
        Cash,
        OptionExercise,
        OptionsExercise,
        Auction,
        OddLot,
        EquityForward,
        EquityCall,
        EquityPut,
        Swap,
        FlexiblePutOption,
        FlexibleCallOption,
        Indicators,
        Curves,
        Surfaces,
        SecurityLendingOtc
    }

    public enum Side
    {
        Buy = 1,
        Sell = 2,
        Lender = 3,
        Borrower = 4,
        Holder = 5,
        Launcher = 6

    }

    public enum SettlementType
    {
        Netting,
        Gross,
        WithoutFinancialTransfer,
        BetweenParts,
        LA,
        LPDE,
        LPD,
        LPDP
    }

    public enum YesOrNoIndicator
    {
        Yes,
        No
    }

    public enum ContractType
    {

        RegularlenderOffer,
        RegularBorrowerOffer,
        RegularDirect,
        MandatoryLoan,
        NonStandard,
        Renew,
        CorporateAction,
        SecLendingSettlementFailure
    }


    [DataContract]
    public class FileImbarqFile
    {
        [DataMember]
        public int ID { get; set; }

        [DataMember]
        public int LayoutID { get; set; }

        [DataMember]
        public DateTime MovDate { get; set; }

        [DataMember]
        public string FileName { get; set; }

        [DataMember]
        public string User { get; set; }

        [DataMember]
        public DateTime InclusionDate { get; set; }
    }

    [DataContract]
    public class FileImbarq
    {

        public Header Header { get; set; }
        public Trailer Trailer { get; set; }
        public List<FileImbarqPositionCashMarket> FileImbarqPositionCashMarkets { get; set; }
        public List<FileImbarqPositionRentalAssets> FileImbarqPositionRentalAssets { get; set; }
        public List<FileImbarqBalanceCustody> FileImbarqBalanceCustodies { get; set; }
    }

    [DataContract]
    public class Header
    {
        [DataMember]
        public int ID { get; set; }

        [DataMember]
        public int RegisterType { get; set; }

        [DataMember]
        public string FileName { get; set; }

        [DataMember]
        public int FileCode { get; set; }

        [DataMember]
        public int UserCategoryCode { get; set; }

        [DataMember]
        public int UserCode { get; set; }

        [DataMember]
        public int DestinationCode { get; set; }

        [DataMember]
        public int SourceCode { get; set; }

        [DataMember]
        public int MovementNumber { get; set; }

        [DataMember]
        public DateTime FileGenerationDate { get; set; }

        [DataMember]
        public string Reservation { get; set; }

        [DataMember]
        public DateTime InclusionDate { get; set; }
    }

    [DataContract]
    public class Trailer : Header
    {
        [DataMember]
        public int TotalRecordsGenerated { get; set; }
    }

    [DataContract]
    public class FileImbarqPositionCashMarket
    {
        [DataMember]
        public int ID { get; set; }

        [DataMember]
        public int RegisterType { get; set; }

        [DataMember]
        public string ParticipantCodeRequester { get; set; }

        [DataMember]
        public string ApplicantInvestorCode { get; set; }

        [DataMember]
        public string RequestedParticipantCode { get; set; }

        [DataMember]
        public string RequestedInvestorCode { get; set; }

        [DataMember]
        public string CustodialCode { get; set; }

        [DataMember]
        public string InvestorCodeCustodian { get; set; }

        [DataMember]
        public string InstrumentCode { get; set; }

        [DataMember]
        public string CodeOriginIdentificationInstrument { get; set; }

        [DataMember]
        public string StockExchangeCode { get; set; }

        [DataMember]
        public string ISIN { get; set; }

        [DataMember]
        public int TradingCode { get; set; }

        [DataMember]
        public string Distribution { get; set; }

        [DataMember]
        public MarketType Market { get; set; }

        [DataMember]
        public int Quotationfactor { get; set; }

        [DataMember]
        public DateTime TradeDate { get; set; }

        [DataMember]
        public DateTime SettlementDate { get; set; }

        [DataMember]
        public string PortfolioAccount { get; set; }

        [DataMember]
        public int QuantityPurchased { get; set; }

        [DataMember]
        public decimal PurchasedFinancialVolume { get; set; }

        [DataMember]
        public decimal AveragePriceBuy { get; set; }

        [DataMember]
        public decimal SoldAmount { get; set; }

        [DataMember]
        public decimal SoldFinancialVolume { get; set; }

        [DataMember]
        public decimal AveragePriceSold { get; set; }

        [DataMember]
        public decimal CoveredPositionSold { get; set; }

        [DataMember]
        public decimal PositionSoldOut { get; set; }

        [DataMember]
        public string Reservation { get; set; }

        [DataMember]
        public DateTime InclusionDate { get; set; }

    }



    [DataContract]
    public class FileImbarqPositionRentalAssets
    {
        [DataMember]
        public int ID { get; set; }

        [DataMember]
        public int RegisterType { get; set; }

        [DataMember]
        public string ParticipantCodeRequester { get; set; }

        [DataMember]
        public string ApplicantInvestorCode { get; set; }

        [DataMember]
        public string RequestedParticipantCode { get; set; }

        [DataMember]
        public string RequestedInvestorCode { get; set; }

        [DataMember]
        public DateTime? DateMovement { get; set; }

        [DataMember]
        public string InstrumentCode { get; set; }

        [DataMember]
        public string SourceCodeIdentificationInstrument { get; set; }

        [DataMember]
        public string StockExchangeCode { get; set; }

        [DataMember]
        public string Source { get; set; }

        [DataMember]
        public string ContractNumber { get; set; }

        [DataMember]
        public string PreviousContractNumber { get; set; }

        [DataMember]
        public Side NatureSidesGiverSeller { get; set; }

        [DataMember]
        public string InstrumentAssetCodeObject { get; set; }

        [DataMember]
        public string SourceCodeIdentificationInstrumentActiveObject { get; set; }

        [DataMember]
        public string AssetStockExchangeCodeObject { get; set; }

        [DataMember]
        public string ObjectActiveISIN { get; set; }

        [DataMember]
        public string ObjectAssetDistribution { get; set; }

        [DataMember]
        public MarketType Market { get; set; }

        [DataMember]
        public string TradingCode { get; set; }

        [DataMember]
        public DateTime TradingDate { get; set; }

        [DataMember]
        public DateTime DueDate { get; set; }

        [DataMember]
        public DateTime GraceDate { get; set; }

       
        [DataMember]
        public decimal ReferencePriceAssetObject { get; set; }

        [DataMember]
        public int Factor { get; set; }

        [DataMember]
        public int OriginalQuantity { get; set; }

        [DataMember]
        public int SettlementQuantity { get; set; }

        [DataMember]
        public int TotalNumberTitlesSettled { get; set; }

       
      


    }

    [DataContract]
    public class FileImbarqBalanceCustody
    {
        [DataMember]
        public int ID { get; set; }

        [DataMember]
        public int RegisterType { get; set; }

        [DataMember]
        public string ParticipantCodeRequester { get; set; }

        [DataMember]
        public string InvestorDigitRequester { get; set; }


        [DataMember]
        public string InvestorCodeRequester { get; set; }

        [DataMember]
        public int PortfolioAccount { get; set; }

        [DataMember]
        public string AccountDescription { get; set; }

        [DataMember]
        public string ISINCode { get; set; }

        [DataMember]
        public int Distribution { get; set; }

        [DataMember]
        public string CompanyNameIssuing { get; set; }

        [DataMember]
        public string Specification { get; set; }

        [DataMember]
        public decimal QuantityCustodyShares { get; set; }

        [DataMember]
        public decimal QuantitySharesBlocked { get; set; }

        [DataMember]
        public string NegotiationCode { get; set; }

        [DataMember]
        public string AnalyticalBalanceIndicator { get; set; }

        public string AssetType { get; set; }

        [DataMember]
        public string Reservation { get; set; }

        [DataMember]
        public DateTime InclusionDate { get; set; }

    }
