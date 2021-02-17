---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 7f13b1a1a5daad4e7c97de962943bb859f6a09df
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402188"
---
# <span data-ttu-id="d8d19-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d8d19-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="d8d19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d19-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d19-103">Zatrzymuje przepływ pracy, w przypadku który uruchamia zalecaną operację indeksowania.</span><span class="sxs-lookup"><span data-stu-id="d8d19-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="d8d19-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8d19-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8d19-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8d19-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d19-106">Polecenie **cmdlet Stop-AzSqlDatabaseExecuteIndexRecommendation** zatrzymuje przepływ pracy, który uruchamia zalecaną operację indeksu.</span><span class="sxs-lookup"><span data-stu-id="d8d19-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="d8d19-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8d19-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d19-108">Przykład 1. Zatrzymywanie uruchamiania zalecenia dotyczącego indeksu</span><span class="sxs-lookup"><span data-stu-id="d8d19-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="d8d19-109">To polecenie przestanie działać z zaleceniem indeksu.</span><span class="sxs-lookup"><span data-stu-id="d8d19-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="d8d19-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d19-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d19-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8d19-111">-DatabaseName</span></span>
<span data-ttu-id="d8d19-112">Określa nazwę bazy danych, dla której to polecenie cmdlet zatrzyma przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="d8d19-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="d8d19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d19-113">-DefaultProfile</span></span>
<span data-ttu-id="d8d19-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d8d19-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8d19-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="d8d19-115">-IndexRecommendationName</span></span>
<span data-ttu-id="d8d19-116">Określa nazwę indeksu, dla których to polecenie cmdlet ma się zatrzymać.</span><span class="sxs-lookup"><span data-stu-id="d8d19-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d8d19-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d19-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8d19-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="d8d19-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d8d19-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8d19-119">-ServerName</span></span>
<span data-ttu-id="d8d19-120">Określa serwer hostowany bazę danych, dla której to polecenie cmdlet zatrzyma przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="d8d19-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="d8d19-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d19-121">CommonParameters</span></span>
<span data-ttu-id="d8d19-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d19-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d19-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8d19-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d19-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8d19-124">INPUTS</span></span>

### <span data-ttu-id="d8d19-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d8d19-125">System.String</span></span>

## <span data-ttu-id="d8d19-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8d19-126">OUTPUTS</span></span>

### <span data-ttu-id="d8d19-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d8d19-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="d8d19-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8d19-128">NOTES</span></span>

## <span data-ttu-id="d8d19-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8d19-129">RELATED LINKS</span></span>


[<span data-ttu-id="d8d19-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="d8d19-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="d8d19-131">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d8d19-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


