---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054753"
---
# <span data-ttu-id="cbc31-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="cbc31-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="cbc31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbc31-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc31-103">Aktualizuje ustawienia sieci wirtualnej usługi w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc31-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="cbc31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbc31-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cbc31-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cbc31-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc31-106">Polecenie cmdlet **Set-AzureVNetConfig** aktualizuje konfigurację sieci dla bieżącej subskrypcji platformy Azure przez określenie ścieżki do pliku konfiguracji sieciowej (netcfg).</span><span class="sxs-lookup"><span data-stu-id="cbc31-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="cbc31-107">W pliku konfiguracji sieci zdefiniowano serwery DNS i podsieci dla usług w chmurze w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="cbc31-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="cbc31-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbc31-108">EXAMPLES</span></span>

### <span data-ttu-id="cbc31-109">Przykład 1: aktualizowanie konfiguracji sieci subskrypcji platformy Azure do pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="cbc31-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="cbc31-110">To polecenie aktualizuje konfigurację sieciową bieżącej subskrypcji platformy Microsoft Azure w pliku lokalnym "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="cbc31-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="cbc31-111">Przykład 2: Ustawianie subskrypcji platformy Azure, a następnie aktualizowanie konfiguracji sieci</span><span class="sxs-lookup"><span data-stu-id="cbc31-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="cbc31-112">W tym przykładzie ustawiono subskrypcję platformy Microsoft Azure, a następnie Zaktualizowano konfigurację sieciową tej subskrypcji, korzystając z konfiguracji zdefiniowanej w pliku lokalnym "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="cbc31-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="cbc31-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbc31-113">PARAMETERS</span></span>

### <span data-ttu-id="cbc31-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="cbc31-114">-ConfigurationPath</span></span>
<span data-ttu-id="cbc31-115">Określa ścieżkę i nazwę pliku konfiguracji sieciowej (netcfg).</span><span class="sxs-lookup"><span data-stu-id="cbc31-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc31-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cbc31-116">-InformationAction</span></span>
<span data-ttu-id="cbc31-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="cbc31-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cbc31-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="cbc31-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbc31-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="cbc31-119">Continue</span></span>
- <span data-ttu-id="cbc31-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="cbc31-120">Ignore</span></span>
- <span data-ttu-id="cbc31-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="cbc31-121">Inquire</span></span>
- <span data-ttu-id="cbc31-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cbc31-122">SilentlyContinue</span></span>
- <span data-ttu-id="cbc31-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="cbc31-123">Stop</span></span>
- <span data-ttu-id="cbc31-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="cbc31-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc31-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cbc31-125">-InformationVariable</span></span>
<span data-ttu-id="cbc31-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="cbc31-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc31-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="cbc31-127">-Profile</span></span>
<span data-ttu-id="cbc31-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbc31-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbc31-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cbc31-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc31-130">CommonParameters</span></span>
<span data-ttu-id="cbc31-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc31-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbc31-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc31-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbc31-133">INPUTS</span></span>

## <span data-ttu-id="cbc31-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbc31-134">OUTPUTS</span></span>

## <span data-ttu-id="cbc31-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbc31-135">NOTES</span></span>

## <span data-ttu-id="cbc31-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbc31-136">RELATED LINKS</span></span>

[<span data-ttu-id="cbc31-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="cbc31-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="cbc31-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="cbc31-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="cbc31-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="cbc31-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


