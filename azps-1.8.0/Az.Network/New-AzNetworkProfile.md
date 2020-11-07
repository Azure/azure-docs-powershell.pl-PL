---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: 87d753ebaf2d8d4891fc96dbc25f7ad0fa1095af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709273"
---
# <span data-ttu-id="f384f-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f384f-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="f384f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f384f-102">SYNOPSIS</span></span>
<span data-ttu-id="f384f-103">Tworzy nowy profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="f384f-103">Creates a new network profile.</span></span>

## <span data-ttu-id="f384f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f384f-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f384f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f384f-105">DESCRIPTION</span></span>
<span data-ttu-id="f384f-106">Polecenie cmdlet **New-AzNetworkProfile** tworzy nowy zasób najwyższego poziomu profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f384f-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="f384f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f384f-107">EXAMPLES</span></span>

### <span data-ttu-id="f384f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f384f-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="f384f-109">Spowoduje to utworzenie nowego zasobu najwyższego poziomu profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="f384f-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="f384f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f384f-110">PARAMETERS</span></span>

### <span data-ttu-id="f384f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f384f-111">-AsJob</span></span>
<span data-ttu-id="f384f-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f384f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f384f-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f384f-113">-ContainerNicConfig</span></span>
<span data-ttu-id="f384f-114">Konfiguracja interfejsu sieciowego kontenera do dodania do tego profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f384f-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="f384f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f384f-115">-DefaultProfile</span></span>
<span data-ttu-id="f384f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f384f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f384f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f384f-117">-Force</span></span>
<span data-ttu-id="f384f-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="f384f-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f384f-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f384f-119">-Location</span></span>
<span data-ttu-id="f384f-120">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f384f-120">The location.</span></span>

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

### <span data-ttu-id="f384f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f384f-121">-Name</span></span>
<span data-ttu-id="f384f-122">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f384f-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="f384f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f384f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f384f-124">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f384f-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="f384f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f384f-125">-Tag</span></span>
<span data-ttu-id="f384f-126">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f384f-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f384f-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f384f-127">-Confirm</span></span>
<span data-ttu-id="f384f-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f384f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f384f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f384f-129">-WhatIf</span></span>
<span data-ttu-id="f384f-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f384f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f384f-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f384f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f384f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f384f-132">CommonParameters</span></span>
<span data-ttu-id="f384f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f384f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f384f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f384f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f384f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f384f-135">INPUTS</span></span>

### <span data-ttu-id="f384f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f384f-136">System.String</span></span>

### <span data-ttu-id="f384f-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f384f-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f384f-138">Microsoft. Azure. Commands. Network. models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f384f-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="f384f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f384f-139">OUTPUTS</span></span>

### <span data-ttu-id="f384f-140">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f384f-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="f384f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f384f-141">NOTES</span></span>

## <span data-ttu-id="f384f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f384f-142">RELATED LINKS</span></span>

[<span data-ttu-id="f384f-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f384f-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="f384f-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f384f-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="f384f-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f384f-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
