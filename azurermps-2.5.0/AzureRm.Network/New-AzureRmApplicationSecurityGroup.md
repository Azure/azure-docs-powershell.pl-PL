---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 99c863861bdf6a434e1268dcb1d9dd55ff8d9f80
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897570"
---
# <span data-ttu-id="86890-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86890-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="86890-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86890-102">SYNOPSIS</span></span>
<span data-ttu-id="86890-103">Tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="86890-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86890-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86890-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86890-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86890-105">DESCRIPTION</span></span>
<span data-ttu-id="86890-106">Polecenie cmdlet **New-AzureRmApplicationSecurityGroup** tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="86890-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="86890-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86890-107">EXAMPLES</span></span>

### <span data-ttu-id="86890-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86890-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="86890-109">W tym przykładzie jest tworzona Grupa zabezpieczeń aplikacji bez żadnych skojarzeń.</span><span class="sxs-lookup"><span data-stu-id="86890-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="86890-110">Po jego utworzeniu w grupie mogą wchodzić konfiguracje IP w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="86890-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="86890-111">Reguły bezpieczeństwa mogą również odwoływać się do grupy jako jej źródeł lub lokalizacji docelowych.</span><span class="sxs-lookup"><span data-stu-id="86890-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="86890-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86890-112">PARAMETERS</span></span>

### <span data-ttu-id="86890-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86890-113">-AsJob</span></span>
<span data-ttu-id="86890-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="86890-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86890-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86890-115">-DefaultProfile</span></span>
<span data-ttu-id="86890-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86890-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86890-117">-Force</span><span class="sxs-lookup"><span data-stu-id="86890-117">-Force</span></span>
<span data-ttu-id="86890-118">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób.</span><span class="sxs-lookup"><span data-stu-id="86890-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="86890-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86890-119">-Location</span></span>
<span data-ttu-id="86890-120">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="86890-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86890-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86890-121">-Name</span></span>
<span data-ttu-id="86890-122">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="86890-122">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86890-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86890-123">-ResourceGroupName</span></span>
<span data-ttu-id="86890-124">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="86890-124">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86890-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="86890-125">-Tag</span></span>
<span data-ttu-id="86890-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="86890-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86890-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86890-127">-Confirm</span></span>
<span data-ttu-id="86890-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86890-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86890-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86890-129">-WhatIf</span></span>
<span data-ttu-id="86890-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86890-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86890-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86890-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86890-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86890-132">CommonParameters</span></span>
<span data-ttu-id="86890-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86890-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86890-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86890-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86890-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86890-135">INPUTS</span></span>

### <span data-ttu-id="86890-136">System. String</span><span class="sxs-lookup"><span data-stu-id="86890-136">System.String</span></span>
<span data-ttu-id="86890-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="86890-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="86890-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86890-138">OUTPUTS</span></span>

### <span data-ttu-id="86890-139">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86890-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="86890-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86890-140">NOTES</span></span>

## <span data-ttu-id="86890-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86890-141">RELATED LINKS</span></span>

[<span data-ttu-id="86890-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86890-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="86890-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86890-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="86890-144">Nowe — AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86890-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="86890-145">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86890-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="86890-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86890-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="86890-147">Nowe — AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="86890-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="86890-148">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="86890-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="86890-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="86890-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
