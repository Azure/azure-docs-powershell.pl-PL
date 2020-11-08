---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052134"
---
# <span data-ttu-id="2f0e3-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2f0e3-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="2f0e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0e3-103">Usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="2f0e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f0e3-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f0e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="2f0e3-106">To polecenie usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="2f0e3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f0e3-107">EXAMPLES</span></span>

### <span data-ttu-id="2f0e3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f0e3-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="2f0e3-109">Usuwa istniejącą regułę sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="2f0e3-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="2f0e3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f0e3-110">PARAMETERS</span></span>

### <span data-ttu-id="2f0e3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f0e3-111">-AsJob</span></span>
<span data-ttu-id="2f0e3-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2f0e3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f0e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0e3-113">-DefaultProfile</span></span>
<span data-ttu-id="2f0e3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f0e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f0e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f0e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="2f0e3-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f0e3-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2f0e3-117">-ServerName</span></span>
<span data-ttu-id="2f0e3-118">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="2f0e3-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="2f0e3-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="2f0e3-120">Nazwa reguły sieci wirtualnej platformy Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="2f0e3-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="2f0e3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f0e3-121">-Confirm</span></span>
<span data-ttu-id="2f0e3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0e3-123">-WhatIf</span></span>
<span data-ttu-id="2f0e3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f0e3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f0e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0e3-126">CommonParameters</span></span>
<span data-ttu-id="2f0e3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0e3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f0e3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0e3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f0e3-129">INPUTS</span></span>

### <span data-ttu-id="2f0e3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f0e3-130">System.String</span></span>

## <span data-ttu-id="2f0e3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f0e3-131">OUTPUTS</span></span>

### <span data-ttu-id="2f0e3-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="2f0e3-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="2f0e3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f0e3-133">NOTES</span></span>

## <span data-ttu-id="2f0e3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f0e3-134">RELATED LINKS</span></span>
