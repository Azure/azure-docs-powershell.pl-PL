---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ac5bf33bd87ff290784728fd0c4857d5278d3057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547843"
---
# <span data-ttu-id="c8eaf-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c8eaf-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="c8eaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="c8eaf-103">Uruchamia przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8eaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8eaf-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8eaf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="c8eaf-106">Polecenie cmdlet **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** uruchamia przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="c8eaf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8eaf-107">EXAMPLES</span></span>

### <span data-ttu-id="c8eaf-108">Przykład 1. Uruchom zalecenie dotyczące indeksu</span><span class="sxs-lookup"><span data-stu-id="c8eaf-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="c8eaf-109">To polecenie uruchamia zalecenie indeksu.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="c8eaf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8eaf-110">PARAMETERS</span></span>

### <span data-ttu-id="c8eaf-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8eaf-111">-DatabaseName</span></span>
<span data-ttu-id="c8eaf-112">Określa nazwę bazy danych, dla której to polecenie cmdlet uruchamia przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8eaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8eaf-113">-DefaultProfile</span></span>
<span data-ttu-id="c8eaf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c8eaf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8eaf-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="c8eaf-115">-IndexRecommendationName</span></span>
<span data-ttu-id="c8eaf-116">Określa nazwę zalecenia dotyczącego indeksu, które zostanie uruchomione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8eaf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8eaf-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8eaf-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8eaf-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c8eaf-119">-ServerName</span></span>
<span data-ttu-id="c8eaf-120">Określa serwer, na którym znajduje się baza danych, dla której ten polecenie cmdlet rozpoczyna przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8eaf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8eaf-121">CommonParameters</span></span>
<span data-ttu-id="c8eaf-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8eaf-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8eaf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8eaf-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8eaf-124">INPUTS</span></span>

### <span data-ttu-id="c8eaf-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c8eaf-125">None</span></span>
<span data-ttu-id="c8eaf-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8eaf-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8eaf-127">OUTPUTS</span></span>

## <span data-ttu-id="c8eaf-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8eaf-128">NOTES</span></span>

## <span data-ttu-id="c8eaf-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8eaf-129">RELATED LINKS</span></span>

[<span data-ttu-id="c8eaf-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="c8eaf-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="c8eaf-131">Zatrzymaj — AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c8eaf-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="c8eaf-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c8eaf-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


