---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062018"
---
# <span data-ttu-id="87ef6-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="87ef6-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="87ef6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="87ef6-103">Zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="87ef6-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="87ef6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87ef6-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87ef6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="87ef6-106">Polecenie cmdlet **stop-AzSqlDatabaseExecuteIndexRecommendation** zatrzymuje przepływ pracy, w którym jest uruchamiana zalecana operacja indeksowania.</span><span class="sxs-lookup"><span data-stu-id="87ef6-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="87ef6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="87ef6-108">Przykład 1: zatrzymywanie działania indeksu zalecenie</span><span class="sxs-lookup"><span data-stu-id="87ef6-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="87ef6-109">To polecenie przestanie działać zalecenie dotyczące indeksu.</span><span class="sxs-lookup"><span data-stu-id="87ef6-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="87ef6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87ef6-110">PARAMETERS</span></span>

### <span data-ttu-id="87ef6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="87ef6-111">-DatabaseName</span></span>
<span data-ttu-id="87ef6-112">Określa nazwę bazy danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="87ef6-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="87ef6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ef6-113">-DefaultProfile</span></span>
<span data-ttu-id="87ef6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87ef6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87ef6-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="87ef6-115">-IndexRecommendationName</span></span>
<span data-ttu-id="87ef6-116">Określa nazwę zalecenia dotyczącego indeksu, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ef6-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="87ef6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ef6-117">-ResourceGroupName</span></span>
<span data-ttu-id="87ef6-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="87ef6-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="87ef6-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="87ef6-119">-ServerName</span></span>
<span data-ttu-id="87ef6-120">Określa serwer hostujący bazę danych, dla której to polecenie cmdlet ma zatrzymywany przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="87ef6-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="87ef6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ef6-121">CommonParameters</span></span>
<span data-ttu-id="87ef6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ef6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ef6-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87ef6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ef6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87ef6-124">INPUTS</span></span>

### <span data-ttu-id="87ef6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="87ef6-125">System.String</span></span>

## <span data-ttu-id="87ef6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87ef6-126">OUTPUTS</span></span>

### <span data-ttu-id="87ef6-127">Microsoft. Azure. Commands. SQL. model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="87ef6-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="87ef6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87ef6-128">NOTES</span></span>

## <span data-ttu-id="87ef6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87ef6-129">RELATED LINKS</span></span>

[<span data-ttu-id="87ef6-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="87ef6-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="87ef6-131">Start — AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="87ef6-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="87ef6-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="87ef6-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


