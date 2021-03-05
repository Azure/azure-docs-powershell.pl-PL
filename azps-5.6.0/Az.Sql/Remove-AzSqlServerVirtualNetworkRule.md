---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 766a5bb6777d1c1ef1e077d4345b7034ede82599
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995149"
---
# <span data-ttu-id="c0b30-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c0b30-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c0b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0b30-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b30-103">Usuwa regułę wirtualnej sieci programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0b30-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c0b30-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0b30-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0b30-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0b30-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b30-106">To polecenie usuwa wirtualną regułę sieciową programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c0b30-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c0b30-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0b30-107">EXAMPLES</span></span>

### <span data-ttu-id="c0b30-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0b30-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="c0b30-109">Usuwa istniejącą regułę sieci wirtualnej programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c0b30-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c0b30-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0b30-110">PARAMETERS</span></span>

### <span data-ttu-id="c0b30-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c0b30-111">-AsJob</span></span>
<span data-ttu-id="c0b30-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c0b30-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b30-113">-DefaultProfile</span></span>
<span data-ttu-id="c0b30-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c0b30-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0b30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b30-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0b30-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0b30-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0b30-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c0b30-117">-ServerName</span></span>
<span data-ttu-id="c0b30-118">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="c0b30-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c0b30-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c0b30-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c0b30-120">Nazwa reguły wirtualnej sieci programu Azure Sql Server</span><span class="sxs-lookup"><span data-stu-id="c0b30-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="c0b30-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0b30-121">-Confirm</span></span>
<span data-ttu-id="c0b30-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0b30-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b30-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b30-123">-WhatIf</span></span>
<span data-ttu-id="c0b30-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0b30-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0b30-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0b30-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b30-126">CommonParameters</span></span>
<span data-ttu-id="c0b30-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0b30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b30-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0b30-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b30-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0b30-129">INPUTS</span></span>

### <span data-ttu-id="c0b30-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c0b30-130">System.String</span></span>

## <span data-ttu-id="c0b30-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0b30-131">OUTPUTS</span></span>

### <span data-ttu-id="c0b30-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c0b30-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c0b30-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0b30-133">NOTES</span></span>

## <span data-ttu-id="c0b30-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0b30-134">RELATED LINKS</span></span>
