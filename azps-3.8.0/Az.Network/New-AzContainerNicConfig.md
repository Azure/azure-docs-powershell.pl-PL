---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 75f05c76b76f37e936798766d9288ace38d1397f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053724"
---
# <span data-ttu-id="d261a-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d261a-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="d261a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d261a-102">SYNOPSIS</span></span>
<span data-ttu-id="d261a-103">Tworzy nowy obiekt konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d261a-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="d261a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d261a-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d261a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d261a-105">DESCRIPTION</span></span>
<span data-ttu-id="d261a-106">Polecenie cmdlet **New-AzContainerNicConfig** tworzy nowy obiekt konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d261a-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="d261a-107">Ten obiekt Określa charakterystyki interfejsu sieci kontenera utworzonego w odwołującym się do nadrzędnego profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="d261a-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="d261a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d261a-108">EXAMPLES</span></span>

### <span data-ttu-id="d261a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d261a-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="d261a-110">Pierwsze polecenie powoduje utworzenie pustej konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d261a-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="d261a-111">Drugi tworzy nowy profil sieciowy, przekazując wcześniej utworzoną konfigurację interfejsu sieciowego kontenera jako argument polecenia cmdlet New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d261a-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="d261a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d261a-112">PARAMETERS</span></span>

### <span data-ttu-id="d261a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d261a-113">-DefaultProfile</span></span>
<span data-ttu-id="d261a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d261a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d261a-115">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d261a-115">-IpConfiguration</span></span>
<span data-ttu-id="d261a-116">Kolekcja profili konfiguracji IP, które określają, jakie konfiguracje IP są tworzone po utworzeniu wystąpienia karty interfejsu sieciowego kontenera na podstawie konfiguracji interfejsu sieciowego kontenera</span><span class="sxs-lookup"><span data-stu-id="d261a-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

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

### <span data-ttu-id="d261a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d261a-117">-Name</span></span>
<span data-ttu-id="d261a-118">Nazwa konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d261a-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="d261a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d261a-119">-Confirm</span></span>
<span data-ttu-id="d261a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d261a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d261a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d261a-121">-WhatIf</span></span>
<span data-ttu-id="d261a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d261a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d261a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d261a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d261a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d261a-124">CommonParameters</span></span>
<span data-ttu-id="d261a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d261a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d261a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d261a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d261a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d261a-127">INPUTS</span></span>

### <span data-ttu-id="d261a-128">Microsoft. Azure. Commands. Network. models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="d261a-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="d261a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d261a-129">OUTPUTS</span></span>

### <span data-ttu-id="d261a-130">Microsoft. Azure. Commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d261a-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="d261a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d261a-131">NOTES</span></span>

## <span data-ttu-id="d261a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d261a-132">RELATED LINKS</span></span>

[<span data-ttu-id="d261a-133">Nowe — AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d261a-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
