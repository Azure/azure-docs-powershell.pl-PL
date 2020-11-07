---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 18d5891e07dd9d0f9916ebf43e8967152e2c9cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709330"
---
# <span data-ttu-id="69142-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="69142-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="69142-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69142-102">SYNOPSIS</span></span>
<span data-ttu-id="69142-103">Tworzy nowy obiekt konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="69142-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="69142-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69142-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69142-105">Opis</span><span class="sxs-lookup"><span data-stu-id="69142-105">DESCRIPTION</span></span>
<span data-ttu-id="69142-106">Polecenie cmdlet **New-AzContainerNicConfig** tworzy nowy obiekt konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="69142-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="69142-107">Ten obiekt Określa charakterystyki sieci interfacs, która utworzyła odwołanie do nadrzędnego profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="69142-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="69142-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69142-108">EXAMPLES</span></span>

### <span data-ttu-id="69142-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69142-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="69142-110">Pierwsze polecenie powoduje utworzenie pustej konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="69142-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="69142-111">Drugi tworzy nowy profil sieciowy, przekazując wcześniej utworzoną konfigurację interfejsu sieciowego kontenera jako argument polecenia cmdlet New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="69142-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="69142-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69142-112">PARAMETERS</span></span>

### <span data-ttu-id="69142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69142-113">-DefaultProfile</span></span>
<span data-ttu-id="69142-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69142-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69142-115">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="69142-115">-IpConfiguration</span></span>
<span data-ttu-id="69142-116">Kolekcja profili konfiguracji IP, które określają, jakie konfiguracje IP są tworzone po utworzeniu wystąpienia karty interfejsu sieciowego kontenera na podstawie konfiguracji interfejsu sieciowego kontenera</span><span class="sxs-lookup"><span data-stu-id="69142-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

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

### <span data-ttu-id="69142-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69142-117">-Name</span></span>
<span data-ttu-id="69142-118">Nazwa konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="69142-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="69142-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69142-119">-Confirm</span></span>
<span data-ttu-id="69142-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69142-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69142-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69142-121">-WhatIf</span></span>
<span data-ttu-id="69142-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69142-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69142-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69142-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69142-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69142-124">CommonParameters</span></span>
<span data-ttu-id="69142-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69142-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69142-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69142-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69142-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69142-127">INPUTS</span></span>

### <span data-ttu-id="69142-128">Microsoft. Azure. Commands. Network. models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="69142-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="69142-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69142-129">OUTPUTS</span></span>

### <span data-ttu-id="69142-130">Microsoft. Azure. Commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="69142-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="69142-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69142-131">NOTES</span></span>

## <span data-ttu-id="69142-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69142-132">RELATED LINKS</span></span>

[<span data-ttu-id="69142-133">Nowe — AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="69142-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
