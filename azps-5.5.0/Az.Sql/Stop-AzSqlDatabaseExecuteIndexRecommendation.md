---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: ca7aeed13627bba3c380b3f1062ee80fcc7c3ebf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241930"
---
# <span data-ttu-id="8541d-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="8541d-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="8541d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8541d-102">SYNOPSIS</span></span>
<span data-ttu-id="8541d-103">Zatrzymuje przepływ pracy, w przypadku który uruchamia zalecaną operację indeksowania.</span><span class="sxs-lookup"><span data-stu-id="8541d-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="8541d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8541d-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8541d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8541d-105">DESCRIPTION</span></span>
<span data-ttu-id="8541d-106">Polecenie **cmdlet Stop-AzSqlDatabaseExecuteIndexRecommendation** zatrzymuje przepływ pracy, który uruchamia zalecaną operację indeksu.</span><span class="sxs-lookup"><span data-stu-id="8541d-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="8541d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8541d-107">EXAMPLES</span></span>

### <span data-ttu-id="8541d-108">Przykład 1. Zatrzymywanie uruchamiania zalecenia dotyczącego indeksu</span><span class="sxs-lookup"><span data-stu-id="8541d-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="8541d-109">To polecenie przestanie działać z zaleceniem indeksu.</span><span class="sxs-lookup"><span data-stu-id="8541d-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="8541d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8541d-110">PARAMETERS</span></span>

### <span data-ttu-id="8541d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8541d-111">-DatabaseName</span></span>
<span data-ttu-id="8541d-112">Określa nazwę bazy danych, dla której to polecenie cmdlet zatrzyma przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="8541d-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="8541d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8541d-113">-DefaultProfile</span></span>
<span data-ttu-id="8541d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8541d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8541d-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="8541d-115">-IndexRecommendationName</span></span>
<span data-ttu-id="8541d-116">Określa nazwę indeksu, dla których to polecenie cmdlet ma się zatrzymać.</span><span class="sxs-lookup"><span data-stu-id="8541d-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="8541d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8541d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8541d-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="8541d-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8541d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8541d-119">-ServerName</span></span>
<span data-ttu-id="8541d-120">Określa serwer hostowany bazę danych, dla której to polecenie cmdlet zatrzyma przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="8541d-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="8541d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8541d-121">CommonParameters</span></span>
<span data-ttu-id="8541d-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8541d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8541d-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8541d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8541d-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8541d-124">INPUTS</span></span>

### <span data-ttu-id="8541d-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8541d-125">System.String</span></span>

## <span data-ttu-id="8541d-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8541d-126">OUTPUTS</span></span>

### <span data-ttu-id="8541d-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="8541d-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="8541d-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8541d-128">NOTES</span></span>

## <span data-ttu-id="8541d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8541d-129">RELATED LINKS</span></span>

[<span data-ttu-id="8541d-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="8541d-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="8541d-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="8541d-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="8541d-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8541d-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


