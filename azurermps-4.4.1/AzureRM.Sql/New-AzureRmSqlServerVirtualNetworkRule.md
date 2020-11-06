---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527205"
---
# <span data-ttu-id="c7f8e-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c7f8e-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c7f8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f8e-103">Umożliwia utworzenie reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7f8e-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7f8e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7f8e-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f8e-106">Umożliwia utworzenie reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="c7f8e-107">Reguły sieci wirtualnej są używane do nawiązywania połączenia z usługą Azure SQL Server z określoną siecią wirtualną w celu ograniczenia dostępu w usłudze Azure SQL Server tylko w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="c7f8e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7f8e-108">EXAMPLES</span></span>

### <span data-ttu-id="c7f8e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7f8e-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="c7f8e-110">Tworzenie reguły sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c7f8e-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c7f8e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7f8e-111">PARAMETERS</span></span>

### <span data-ttu-id="c7f8e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f8e-112">-ResourceGroupName</span></span>
<span data-ttu-id="c7f8e-113">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="c7f8e-114">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c7f8e-114">-ServerName</span></span>
<span data-ttu-id="c7f8e-115">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c7f8e-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c7f8e-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c7f8e-117">Nazwa reguły sieci wirtualnej platformy Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="c7f8e-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="c7f8e-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="c7f8e-119">Identyfikator podsieci sieci wirtualnej określający dane firmy Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="c7f8e-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="c7f8e-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7f8e-120">-Confirm</span></span>
<span data-ttu-id="c7f8e-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7f8e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7f8e-122">-WhatIf</span></span>
<span data-ttu-id="c7f8e-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7f8e-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7f8e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f8e-125">-DefaultProfile</span></span>
<span data-ttu-id="c7f8e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f8e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f8e-127">CommonParameters</span></span>
<span data-ttu-id="c7f8e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f8e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f8e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f8e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f8e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7f8e-130">INPUTS</span></span>

### <span data-ttu-id="c7f8e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c7f8e-131">System.String</span></span>

## <span data-ttu-id="c7f8e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7f8e-132">OUTPUTS</span></span>

### <span data-ttu-id="c7f8e-133">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c7f8e-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c7f8e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7f8e-134">NOTES</span></span>

## <span data-ttu-id="c7f8e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7f8e-135">RELATED LINKS</span></span>

