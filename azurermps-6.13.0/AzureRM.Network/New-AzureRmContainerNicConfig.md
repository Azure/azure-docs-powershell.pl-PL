---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719400"
---
# <span data-ttu-id="463fc-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="463fc-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="463fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="463fc-102">SYNOPSIS</span></span>
<span data-ttu-id="463fc-103">Tworzy nowy obiekt konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="463fc-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="463fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="463fc-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="463fc-105">DESCRIPTION</span></span>
<span data-ttu-id="463fc-106">Polecenie cmdlet **New-AzureRmNetworkProfileContainerNicConfig** tworzy nowy obiekt konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="463fc-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="463fc-107">Ten obiekt Określa charakterystyki sieci interfacs, która utworzyła odwołanie do nadrzędnego profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="463fc-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="463fc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="463fc-108">EXAMPLES</span></span>

### <span data-ttu-id="463fc-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="463fc-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="463fc-110">Pierwsze polecenie powoduje utworzenie pustej konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="463fc-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="463fc-111">Drugi tworzy nowy profil sieciowy, przekazując wcześniej utworzoną konfigurację interfejsu sieciowego kontenera jako argument polecenia cmdlet New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="463fc-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="463fc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="463fc-112">PARAMETERS</span></span>

### <span data-ttu-id="463fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463fc-113">-DefaultProfile</span></span>
<span data-ttu-id="463fc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="463fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463fc-115">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="463fc-115">-IpConfiguration</span></span>
<span data-ttu-id="463fc-116">{{Opis elementu IpConfiguration wypełnienia}}</span><span class="sxs-lookup"><span data-stu-id="463fc-116">{{Fill IpConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="463fc-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="463fc-117">-Name</span></span>
<span data-ttu-id="463fc-118">Nazwa konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="463fc-118">Name of the container network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="463fc-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="463fc-119">-Confirm</span></span>
<span data-ttu-id="463fc-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463fc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463fc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463fc-121">-WhatIf</span></span>
<span data-ttu-id="463fc-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="463fc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="463fc-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="463fc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463fc-124">CommonParameters</span></span>
<span data-ttu-id="463fc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463fc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463fc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463fc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="463fc-127">INPUTS</span></span>

### <span data-ttu-id="463fc-128">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSIPConfigurationProfile; Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="463fc-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="463fc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="463fc-129">OUTPUTS</span></span>

### <span data-ttu-id="463fc-130">Microsoft. Azure. Commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="463fc-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="463fc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="463fc-131">NOTES</span></span>

## <span data-ttu-id="463fc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="463fc-132">RELATED LINKS</span></span>
