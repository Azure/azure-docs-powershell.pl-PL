---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 3e9b99a1ab9d3fdce813166e7a0834c14b81b651
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886890"
---
# <span data-ttu-id="1c3dd-101">Get-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1c3dd-101">Get-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="1c3dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3dd-103">Pobiera lub wyświetla regułę wirtualnej sieci programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="1c3dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c3dd-104">SYNTAX</span></span>

```
Get-AzSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c3dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3dd-106">To polecenie pobiera określoną regułę sieci wirtualnej usługi Azure SQL Server lub listę reguł wirtualnej sieci usługi Azure SQL Server w obszarze serwera.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="1c3dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c3dd-107">EXAMPLES</span></span>

### <span data-ttu-id="1c3dd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c3dd-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="1c3dd-109">Pobiera pojedynczą regułę sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1c3dd-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="1c3dd-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1c3dd-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="1c3dd-111">Pobiera listę reguł wirtualnej sieci programu Azure SQL Server w ramach określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

### <span data-ttu-id="1c3dd-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1c3dd-112">Example 3</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRule*
```

<span data-ttu-id="1c3dd-113">Pobiera listę reguł sieci wirtualnej usługi Azure SQL Server na określonym serwerze, który rozpoczyna się od "virtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="1c3dd-113">Gets the list of Azure SQL Server virtual network rules under the specified server that start with "virtualNetworkRule".</span></span>

## <span data-ttu-id="1c3dd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c3dd-114">PARAMETERS</span></span>

### <span data-ttu-id="1c3dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3dd-115">-DefaultProfile</span></span>
<span data-ttu-id="1c3dd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1c3dd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c3dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c3dd-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c3dd-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1c3dd-119">-ServerName</span></span>
<span data-ttu-id="1c3dd-120">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1c3dd-121">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="1c3dd-121">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="1c3dd-122">Nazwa reguły sieci wirtualnej platformy Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-122">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1c3dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3dd-123">CommonParameters</span></span>
<span data-ttu-id="1c3dd-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3dd-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c3dd-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3dd-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c3dd-126">INPUTS</span></span>

### <span data-ttu-id="1c3dd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1c3dd-127">System.String</span></span>

## <span data-ttu-id="1c3dd-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c3dd-128">OUTPUTS</span></span>

### <span data-ttu-id="1c3dd-129">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="1c3dd-129">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="1c3dd-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c3dd-130">NOTES</span></span>

## <span data-ttu-id="1c3dd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c3dd-131">RELATED LINKS</span></span>
