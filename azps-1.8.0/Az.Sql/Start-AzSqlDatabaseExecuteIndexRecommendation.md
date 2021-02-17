---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 1ab1e223ec173cf5727011956f52979026159594
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399519"
---
# <span data-ttu-id="ea78e-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ea78e-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="ea78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea78e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea78e-103">Uruchamia przepływ pracy, w przypadku który uruchamia zalecaną operację indeksowania.</span><span class="sxs-lookup"><span data-stu-id="ea78e-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="ea78e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea78e-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea78e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea78e-105">DESCRIPTION</span></span>
<span data-ttu-id="ea78e-106">Polecenie **cmdlet Start-AzSqlDatabaseExecuteIndexRecommendation** uruchamia przepływ pracy, który uruchamia zalecaną operację indeksowania dla usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="ea78e-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="ea78e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea78e-107">EXAMPLES</span></span>

### <span data-ttu-id="ea78e-108">Przykład 1. Uruchamianie zalecenia dotyczącego indeksu</span><span class="sxs-lookup"><span data-stu-id="ea78e-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ea78e-109">To polecenie uruchamia zalecenie indeksu.</span><span class="sxs-lookup"><span data-stu-id="ea78e-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="ea78e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea78e-110">PARAMETERS</span></span>

### <span data-ttu-id="ea78e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea78e-111">-DatabaseName</span></span>
<span data-ttu-id="ea78e-112">Określa nazwę bazy danych, dla której to polecenie cmdlet uruchomi przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="ea78e-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="ea78e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea78e-113">-DefaultProfile</span></span>
<span data-ttu-id="ea78e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ea78e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea78e-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ea78e-115">-IndexRecommendationName</span></span>
<span data-ttu-id="ea78e-116">Określa nazwę indeksu, które ma być uruchamiane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea78e-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="ea78e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea78e-117">-ResourceGroupName</span></span>
<span data-ttu-id="ea78e-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="ea78e-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ea78e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea78e-119">-ServerName</span></span>
<span data-ttu-id="ea78e-120">Określa serwer hostowany bazę danych, dla której to polecenie cmdlet uruchamia przepływ pracy.</span><span class="sxs-lookup"><span data-stu-id="ea78e-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="ea78e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea78e-121">CommonParameters</span></span>
<span data-ttu-id="ea78e-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea78e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea78e-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea78e-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea78e-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea78e-124">INPUTS</span></span>

### <span data-ttu-id="ea78e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ea78e-125">System.String</span></span>

## <span data-ttu-id="ea78e-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea78e-126">OUTPUTS</span></span>

### <span data-ttu-id="ea78e-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ea78e-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ea78e-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea78e-128">NOTES</span></span>

## <span data-ttu-id="ea78e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea78e-129">RELATED LINKS</span></span>


[<span data-ttu-id="ea78e-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ea78e-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ea78e-131">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ea78e-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


