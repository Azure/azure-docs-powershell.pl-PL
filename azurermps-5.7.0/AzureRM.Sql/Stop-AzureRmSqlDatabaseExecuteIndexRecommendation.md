---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717677"
---
# <span data-ttu-id="25bc9-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="25bc9-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="25bc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="25bc9-103">Zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="25bc9-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25bc9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25bc9-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25bc9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="25bc9-106">Polecenie cmdlet **stop-AzureRmSqlDatabaseExecuteIndexRecommendation** zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="25bc9-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="25bc9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25bc9-107">EXAMPLES</span></span>

### <span data-ttu-id="25bc9-108">Przykład 1: zatrzymywanie działania indeksu zalecenie</span><span class="sxs-lookup"><span data-stu-id="25bc9-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="25bc9-109">To polecenie przestanie działać zalecenie dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="25bc9-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="25bc9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25bc9-110">PARAMETERS</span></span>

### <span data-ttu-id="25bc9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25bc9-111">-DatabaseName</span></span>
<span data-ttu-id="25bc9-112">Określa nazwę bazy danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="25bc9-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="25bc9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bc9-113">-DefaultProfile</span></span>
<span data-ttu-id="25bc9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25bc9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25bc9-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="25bc9-115">-IndexRecommendationName</span></span>
<span data-ttu-id="25bc9-116">Określa nazwę zalecenia dotyczącego indeksu, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25bc9-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="25bc9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bc9-117">-ResourceGroupName</span></span>
<span data-ttu-id="25bc9-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="25bc9-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="25bc9-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="25bc9-119">-ServerName</span></span>
<span data-ttu-id="25bc9-120">Określa serwer hostujący bazę danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="25bc9-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="25bc9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bc9-121">CommonParameters</span></span>
<span data-ttu-id="25bc9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bc9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bc9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bc9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bc9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25bc9-124">INPUTS</span></span>

### <span data-ttu-id="25bc9-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="25bc9-125">None</span></span>
<span data-ttu-id="25bc9-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="25bc9-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25bc9-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25bc9-127">OUTPUTS</span></span>

## <span data-ttu-id="25bc9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25bc9-128">NOTES</span></span>

## <span data-ttu-id="25bc9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25bc9-129">RELATED LINKS</span></span>

[<span data-ttu-id="25bc9-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="25bc9-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="25bc9-131">Start — AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="25bc9-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="25bc9-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="25bc9-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


