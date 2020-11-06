---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c0e7bc13d52633a1da5bfac2d9aec38ea3d0ee7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542200"
---
# <span data-ttu-id="075b3-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="075b3-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="075b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="075b3-102">SYNOPSIS</span></span>
<span data-ttu-id="075b3-103">Usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="075b3-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="075b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="075b3-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="075b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="075b3-105">DESCRIPTION</span></span>
<span data-ttu-id="075b3-106">To polecenie usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="075b3-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="075b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="075b3-107">EXAMPLES</span></span>

### <span data-ttu-id="075b3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="075b3-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="075b3-109">Usuwa istniejącą regułę sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="075b3-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="075b3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="075b3-110">PARAMETERS</span></span>

### <span data-ttu-id="075b3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="075b3-111">-AsJob</span></span>
<span data-ttu-id="075b3-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="075b3-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075b3-113">-DefaultProfile</span></span>
<span data-ttu-id="075b3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="075b3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>


```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075b3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="075b3-115">-ResourceGroupName</span></span>
<span data-ttu-id="075b3-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="075b3-116">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="075b3-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="075b3-117">-ServerName</span></span>
<span data-ttu-id="075b3-118">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="075b3-118">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075b3-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="075b3-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="075b3-120">Nazwa reguły sieci wirtualnej platformy Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="075b3-120">Azure Sql Server Virtual Network Rule name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075b3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="075b3-121">-Confirm</span></span>
<span data-ttu-id="075b3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="075b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="075b3-123">-WhatIf</span></span>
<span data-ttu-id="075b3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="075b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="075b3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="075b3-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075b3-126">CommonParameters</span></span>
<span data-ttu-id="075b3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="075b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075b3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="075b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075b3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="075b3-129">INPUTS</span></span>

### <span data-ttu-id="075b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="075b3-130">System.String</span></span>

## <span data-ttu-id="075b3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="075b3-131">OUTPUTS</span></span>

### <span data-ttu-id="075b3-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="075b3-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="075b3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="075b3-133">NOTES</span></span>

## <span data-ttu-id="075b3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="075b3-134">RELATED LINKS</span></span>
