---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895649"
---
# <span data-ttu-id="f6ee3-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f6ee3-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="f6ee3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ee3-103">Zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="f6ee3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6ee3-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6ee3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6ee3-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ee3-106">Polecenie cmdlet **stop-AzSqlDatabaseExecuteIndexRecommendation** zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="f6ee3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6ee3-107">EXAMPLES</span></span>

### <span data-ttu-id="f6ee3-108">Przykład 1: zatrzymywanie działania indeksu zalecenie</span><span class="sxs-lookup"><span data-stu-id="f6ee3-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="f6ee3-109">To polecenie przestanie działać zalecenie dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="f6ee3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6ee3-110">PARAMETERS</span></span>

### <span data-ttu-id="f6ee3-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6ee3-111">-DatabaseName</span></span>
<span data-ttu-id="f6ee3-112">Określa nazwę bazy danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6ee3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ee3-113">-DefaultProfile</span></span>
<span data-ttu-id="f6ee3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f6ee3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6ee3-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="f6ee3-115">-IndexRecommendationName</span></span>
<span data-ttu-id="f6ee3-116">Określa nazwę zalecenia dotyczącego indeksu, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6ee3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ee3-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6ee3-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6ee3-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f6ee3-119">-ServerName</span></span>
<span data-ttu-id="f6ee3-120">Określa serwer hostujący bazę danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6ee3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ee3-121">CommonParameters</span></span>
<span data-ttu-id="f6ee3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ee3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ee3-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6ee3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ee3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6ee3-124">INPUTS</span></span>

### <span data-ttu-id="f6ee3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ee3-125">System.String</span></span>

## <span data-ttu-id="f6ee3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6ee3-126">OUTPUTS</span></span>

### <span data-ttu-id="f6ee3-127">Microsoft. Azure. Commands. SQL. model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f6ee3-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="f6ee3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6ee3-128">NOTES</span></span>

## <span data-ttu-id="f6ee3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6ee3-129">RELATED LINKS</span></span>

[<span data-ttu-id="f6ee3-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f6ee3-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="f6ee3-131">Start — AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="f6ee3-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="f6ee3-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f6ee3-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


