---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f8ac34526691f3bdacdd0736189e063c969f63ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178443"
---
# <span data-ttu-id="d0a87-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d0a87-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="d0a87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a87-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a87-103">Pobiera lub wyświetla wirtualną regułę sieciową programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0a87-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="d0a87-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0a87-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0a87-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0a87-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a87-106">To polecenie pobiera określoną regułę wirtualnej sieci programu Azure SQL Server lub listę reguł sieci wirtualnej programu Azure SQL Server w obszarze serwera.</span><span class="sxs-lookup"><span data-stu-id="d0a87-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="d0a87-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0a87-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a87-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0a87-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="d0a87-109">Pobiera jedną regułę wirtualnej sieci programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="d0a87-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="d0a87-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d0a87-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="d0a87-111">Pobiera listę reguł sieci wirtualnej programu Azure SQL Server pod określony serwer</span><span class="sxs-lookup"><span data-stu-id="d0a87-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="d0a87-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d0a87-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="d0a87-113">Pobiera listę reguł sieci wirtualnej programu Azure SQL Server na określonym serwerze, które zaczynają się od "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="d0a87-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="d0a87-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0a87-114">PARAMETERS</span></span>

### <span data-ttu-id="d0a87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a87-115">-DefaultProfile</span></span>
<span data-ttu-id="d0a87-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d0a87-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0a87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a87-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0a87-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0a87-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0a87-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0a87-119">-ServerName</span></span>
<span data-ttu-id="d0a87-120">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="d0a87-120">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a87-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="d0a87-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="d0a87-122">Nazwa reguły wirtualnej sieci programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="d0a87-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a87-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a87-123">CommonParameters</span></span>
<span data-ttu-id="d0a87-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a87-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a87-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0a87-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a87-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0a87-126">INPUTS</span></span>

### <span data-ttu-id="d0a87-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d0a87-127">System.String</span></span>

## <span data-ttu-id="d0a87-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0a87-128">OUTPUTS</span></span>

### <span data-ttu-id="d0a87-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="d0a87-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="d0a87-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0a87-130">NOTES</span></span>

## <span data-ttu-id="d0a87-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0a87-131">RELATED LINKS</span></span>
