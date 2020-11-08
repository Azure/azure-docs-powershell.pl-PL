---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055183"
---
# <span data-ttu-id="1551a-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1551a-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="1551a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1551a-102">SYNOPSIS</span></span>
<span data-ttu-id="1551a-103">Tworzy mapowanie między sieciami wirtualnymi.</span><span class="sxs-lookup"><span data-stu-id="1551a-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="1551a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1551a-104">SYNTAX</span></span>

### <span data-ttu-id="1551a-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="1551a-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1551a-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="1551a-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1551a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1551a-107">DESCRIPTION</span></span>
<span data-ttu-id="1551a-108">Polecenie cmdlet **New-AzureSiteRecoveryNetworkMapping** tworzy mapowanie między dwiema sieciami wirtualnymi i zwraca zadanie odzyskiwania witryny Azure, aby je śledzić.</span><span class="sxs-lookup"><span data-stu-id="1551a-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="1551a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1551a-109">EXAMPLES</span></span>

### <span data-ttu-id="1551a-110">Przykład 1. Tworzenie mapowania między siecią a siecią odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="1551a-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="1551a-111">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="1551a-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="1551a-112">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="1551a-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="1551a-113">Drugie polecenie pobiera sieć odzyskiwania witryny dla pierwszego serwera w tablicy $Servers przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="1551a-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="1551a-114">Polecenie przechowuje sieci w zmiennej $Networks.</span><span class="sxs-lookup"><span data-stu-id="1551a-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="1551a-115">Ostatnie polecenie tworzy mapowanie między siecią podstawową a siecią odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1551a-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="1551a-116">Polecenie określa podstawową sieć jako pierwszy element $Networks.</span><span class="sxs-lookup"><span data-stu-id="1551a-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="1551a-117">To polecenie określa sieć odzyskiwania jako drugi element $Networks.</span><span class="sxs-lookup"><span data-stu-id="1551a-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="1551a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1551a-118">PARAMETERS</span></span>

### <span data-ttu-id="1551a-119">-AzureSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1551a-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="1551a-120">Określa identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1551a-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1551a-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="1551a-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="1551a-122">Określa identyfikator sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1551a-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1551a-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="1551a-123">-PrimaryNetwork</span></span>
<span data-ttu-id="1551a-124">Określa podstawowy obiekt sieciowy.</span><span class="sxs-lookup"><span data-stu-id="1551a-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1551a-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="1551a-125">-Profile</span></span>
<span data-ttu-id="1551a-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1551a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1551a-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1551a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1551a-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="1551a-128">-RecoveryNetwork</span></span>
<span data-ttu-id="1551a-129">Określa obiekt sieciowy odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1551a-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1551a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1551a-130">CommonParameters</span></span>
<span data-ttu-id="1551a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1551a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1551a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1551a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1551a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1551a-133">INPUTS</span></span>

## <span data-ttu-id="1551a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1551a-134">OUTPUTS</span></span>

## <span data-ttu-id="1551a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1551a-135">NOTES</span></span>

## <span data-ttu-id="1551a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1551a-136">RELATED LINKS</span></span>

[<span data-ttu-id="1551a-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1551a-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="1551a-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1551a-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="1551a-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="1551a-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


