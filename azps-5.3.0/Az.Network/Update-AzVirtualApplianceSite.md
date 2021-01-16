---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490917"
---
# <span data-ttu-id="a28b8-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a28b8-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="a28b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a28b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a28b8-103">Zmienianie lub modyfikowanie witryny urządzenia wirtualnego połączonej z zasobem sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a28b8-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a28b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a28b8-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a28b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a28b8-105">DESCRIPTION</span></span>
<span data-ttu-id="a28b8-106">Polecenie Update-AzVirtualApplianceSite modyfikuje zasób witryny urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="a28b8-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="a28b8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a28b8-107">EXAMPLES</span></span>

### <span data-ttu-id="a28b8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a28b8-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="a28b8-109">Zmodyfikuj prefiks adresu zasobu witryny wirtualnej urządzenia.</span><span class="sxs-lookup"><span data-stu-id="a28b8-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="a28b8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a28b8-110">PARAMETERS</span></span>

### <span data-ttu-id="a28b8-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="a28b8-111">-AddresssPrefix</span></span>
<span data-ttu-id="a28b8-112">Prefiks adresu witryny.</span><span class="sxs-lookup"><span data-stu-id="a28b8-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a28b8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a28b8-113">-AsJob</span></span>
<span data-ttu-id="a28b8-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a28b8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a28b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28b8-115">-DefaultProfile</span></span>
<span data-ttu-id="a28b8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a28b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a28b8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a28b8-117">-Force</span></span>
<span data-ttu-id="a28b8-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="a28b8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a28b8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a28b8-119">-Name</span></span>
<span data-ttu-id="a28b8-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a28b8-120">The resource name.</span></span>

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

### <span data-ttu-id="a28b8-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="a28b8-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="a28b8-122">Sieciowy urządzenie wirtualne, do którego jest dołączona Ta witryna.</span><span class="sxs-lookup"><span data-stu-id="a28b8-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="a28b8-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="a28b8-123">-O365Policy</span></span>
<span data-ttu-id="a28b8-124">Zasady podgrupa pakietu Office 365.</span><span class="sxs-lookup"><span data-stu-id="a28b8-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a28b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a28b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="a28b8-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a28b8-126">The resource group name.</span></span>

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

### <span data-ttu-id="a28b8-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a28b8-127">-Tag</span></span>
<span data-ttu-id="a28b8-128">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="a28b8-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a28b8-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a28b8-129">-Confirm</span></span>
<span data-ttu-id="a28b8-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a28b8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a28b8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a28b8-131">-WhatIf</span></span>
<span data-ttu-id="a28b8-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a28b8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a28b8-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a28b8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a28b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28b8-134">CommonParameters</span></span>
<span data-ttu-id="a28b8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28b8-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a28b8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28b8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a28b8-137">INPUTS</span></span>

### <span data-ttu-id="a28b8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a28b8-138">System.String</span></span>

### <span data-ttu-id="a28b8-139">Microsoft. Azure. Commands. Network. models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="a28b8-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="a28b8-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a28b8-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a28b8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a28b8-141">OUTPUTS</span></span>

### <span data-ttu-id="a28b8-142">Microsoft. Azure. Commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a28b8-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="a28b8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a28b8-143">NOTES</span></span>

## <span data-ttu-id="a28b8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a28b8-144">RELATED LINKS</span></span>
