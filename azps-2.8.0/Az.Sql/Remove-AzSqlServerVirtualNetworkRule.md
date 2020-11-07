---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: de7df0147cc28d413444282987f8d5b27f9607a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887297"
---
# <span data-ttu-id="4a459-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4a459-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="4a459-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a459-102">SYNOPSIS</span></span>
<span data-ttu-id="4a459-103">Usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4a459-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="4a459-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a459-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a459-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a459-105">DESCRIPTION</span></span>
<span data-ttu-id="4a459-106">To polecenie usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4a459-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="4a459-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a459-107">EXAMPLES</span></span>

### <span data-ttu-id="4a459-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a459-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="4a459-109">Usuwa istniejącą regułę sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="4a459-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="4a459-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a459-110">PARAMETERS</span></span>

### <span data-ttu-id="4a459-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a459-111">-AsJob</span></span>
<span data-ttu-id="4a459-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4a459-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a459-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a459-113">-DefaultProfile</span></span>
<span data-ttu-id="4a459-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4a459-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a459-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a459-115">-ResourceGroupName</span></span>
<span data-ttu-id="4a459-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a459-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a459-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4a459-117">-ServerName</span></span>
<span data-ttu-id="4a459-118">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4a459-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4a459-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="4a459-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="4a459-120">Nazwa reguły sieci wirtualnej platformy Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="4a459-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="4a459-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a459-121">-Confirm</span></span>
<span data-ttu-id="4a459-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a459-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a459-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a459-123">-WhatIf</span></span>
<span data-ttu-id="4a459-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a459-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a459-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a459-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a459-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a459-126">CommonParameters</span></span>
<span data-ttu-id="4a459-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a459-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a459-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a459-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a459-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a459-129">INPUTS</span></span>

### <span data-ttu-id="4a459-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a459-130">System.String</span></span>

## <span data-ttu-id="4a459-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a459-131">OUTPUTS</span></span>

### <span data-ttu-id="4a459-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="4a459-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="4a459-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a459-133">NOTES</span></span>

## <span data-ttu-id="4a459-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a459-134">RELATED LINKS</span></span>
