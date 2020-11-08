---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: e463e6a1d25db24553b62c8d2fea1051eb231840
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051028"
---
# <span data-ttu-id="c72c4-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c72c4-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="c72c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c72c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c72c4-103">Tworzy nowy profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="c72c4-103">Creates a new network profile.</span></span>

## <span data-ttu-id="c72c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c72c4-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c72c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c72c4-105">DESCRIPTION</span></span>
<span data-ttu-id="c72c4-106">Polecenie cmdlet **New-AzNetworkProfile** tworzy nowy zasób najwyższego poziomu profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c72c4-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="c72c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c72c4-107">EXAMPLES</span></span>

### <span data-ttu-id="c72c4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c72c4-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="c72c4-109">Spowoduje to utworzenie nowego zasobu najwyższego poziomu profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="c72c4-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="c72c4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c72c4-110">PARAMETERS</span></span>

### <span data-ttu-id="c72c4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c72c4-111">-AsJob</span></span>
<span data-ttu-id="c72c4-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c72c4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c72c4-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c72c4-113">-ContainerNicConfig</span></span>
<span data-ttu-id="c72c4-114">Konfiguracja interfejsu sieciowego kontenera do dodania do tego profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c72c4-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c72c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72c4-115">-DefaultProfile</span></span>
<span data-ttu-id="c72c4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c72c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c72c4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c72c4-117">-Force</span></span>
<span data-ttu-id="c72c4-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="c72c4-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c72c4-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c72c4-119">-Location</span></span>
<span data-ttu-id="c72c4-120">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c72c4-120">The location.</span></span>

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

### <span data-ttu-id="c72c4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c72c4-121">-Name</span></span>
<span data-ttu-id="c72c4-122">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c72c4-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="c72c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c72c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="c72c4-124">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c72c4-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="c72c4-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="c72c4-125">-Tag</span></span>
<span data-ttu-id="c72c4-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="c72c4-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c72c4-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c72c4-127">-Confirm</span></span>
<span data-ttu-id="c72c4-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c72c4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c72c4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c72c4-129">-WhatIf</span></span>
<span data-ttu-id="c72c4-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c72c4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c72c4-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c72c4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c72c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72c4-132">CommonParameters</span></span>
<span data-ttu-id="c72c4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c72c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72c4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c72c4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72c4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c72c4-135">INPUTS</span></span>

### <span data-ttu-id="c72c4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c72c4-136">System.String</span></span>

### <span data-ttu-id="c72c4-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c72c4-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c72c4-138">Microsoft. Azure. Commands. Network. models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="c72c4-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="c72c4-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c72c4-139">OUTPUTS</span></span>

### <span data-ttu-id="c72c4-140">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c72c4-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="c72c4-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c72c4-141">NOTES</span></span>

## <span data-ttu-id="c72c4-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c72c4-142">RELATED LINKS</span></span>

[<span data-ttu-id="c72c4-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c72c4-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="c72c4-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c72c4-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="c72c4-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c72c4-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
