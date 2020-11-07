---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719512"
---
# <span data-ttu-id="c8f4e-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c8f4e-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c8f4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f4e-103">Usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8f4e-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8f4e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8f4e-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f4e-106">To polecenie usuwa regułę sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="c8f4e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8f4e-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f4e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8f4e-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="c8f4e-109">Usuwa istniejącą regułę sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c8f4e-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c8f4e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8f4e-110">PARAMETERS</span></span>

### <span data-ttu-id="c8f4e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-111">-ResourceGroupName</span></span>
<span data-ttu-id="c8f4e-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8f4e-113">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c8f4e-113">-ServerName</span></span>
<span data-ttu-id="c8f4e-114">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c8f4e-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c8f4e-116">Nazwa reguły sieci wirtualnej platformy Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c8f4e-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="c8f4e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8f4e-117">-Confirm</span></span>
<span data-ttu-id="c8f4e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8f4e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f4e-119">-WhatIf</span></span>
<span data-ttu-id="c8f4e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8f4e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8f4e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f4e-122">-DefaultProfile</span></span>
<span data-ttu-id="c8f4e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8f4e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f4e-124">CommonParameters</span></span>
<span data-ttu-id="c8f4e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f4e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f4e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f4e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8f4e-127">INPUTS</span></span>

### <span data-ttu-id="c8f4e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c8f4e-128">System.String</span></span>

## <span data-ttu-id="c8f4e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8f4e-129">OUTPUTS</span></span>

### <span data-ttu-id="c8f4e-130">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c8f4e-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c8f4e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8f4e-131">NOTES</span></span>

## <span data-ttu-id="c8f4e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8f4e-132">RELATED LINKS</span></span>

