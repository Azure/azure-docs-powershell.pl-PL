---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718514"
---
# <span data-ttu-id="cd751-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd751-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="cd751-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd751-102">SYNOPSIS</span></span>
<span data-ttu-id="cd751-103">Tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd751-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd751-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd751-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd751-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd751-105">DESCRIPTION</span></span>
<span data-ttu-id="cd751-106">Polecenie cmdlet **New-AzureRmApplicationSecurityGroup** tworzy grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd751-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="cd751-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd751-107">EXAMPLES</span></span>

### <span data-ttu-id="cd751-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd751-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="cd751-109">W tym przykładzie jest tworzona Grupa zabezpieczeń aplikacji bez żadnych skojarzeń.</span><span class="sxs-lookup"><span data-stu-id="cd751-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="cd751-110">Po jego utworzeniu w grupie mogą wchodzić konfiguracje IP w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="cd751-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="cd751-111">Reguły bezpieczeństwa mogą również odwoływać się do grupy jako jej źródeł lub lokalizacji docelowych.</span><span class="sxs-lookup"><span data-stu-id="cd751-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="cd751-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd751-112">PARAMETERS</span></span>

### <span data-ttu-id="cd751-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd751-113">-DefaultProfile</span></span>
<span data-ttu-id="cd751-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd751-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd751-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd751-115">-Force</span></span>
<span data-ttu-id="cd751-116">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób.</span><span class="sxs-lookup"><span data-stu-id="cd751-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="cd751-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cd751-117">-Location</span></span>
<span data-ttu-id="cd751-118">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cd751-118">The location.</span></span>

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

### <span data-ttu-id="cd751-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd751-119">-Name</span></span>
<span data-ttu-id="cd751-120">Nazwa grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd751-120">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd751-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd751-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd751-122">Nazwa grupy zasobów grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd751-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="cd751-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd751-123">-Tag</span></span>
<span data-ttu-id="cd751-124">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd751-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd751-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd751-125">-Confirm</span></span>
<span data-ttu-id="cd751-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd751-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd751-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd751-127">-WhatIf</span></span>
<span data-ttu-id="cd751-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd751-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd751-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd751-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd751-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd751-130">CommonParameters</span></span>
<span data-ttu-id="cd751-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd751-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd751-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd751-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd751-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd751-133">INPUTS</span></span>

### <span data-ttu-id="cd751-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd751-134">System.String</span></span>
<span data-ttu-id="cd751-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd751-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cd751-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd751-136">OUTPUTS</span></span>

### <span data-ttu-id="cd751-137">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd751-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="cd751-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd751-138">NOTES</span></span>

## <span data-ttu-id="cd751-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd751-139">RELATED LINKS</span></span>

[<span data-ttu-id="cd751-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd751-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="cd751-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cd751-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="cd751-142">Nowe — AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd751-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cd751-143">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd751-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cd751-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd751-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cd751-145">Nowe — AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd751-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cd751-146">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd751-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cd751-147">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd751-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
