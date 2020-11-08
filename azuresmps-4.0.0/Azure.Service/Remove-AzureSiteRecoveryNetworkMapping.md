---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055076"
---
# <span data-ttu-id="b5422-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b5422-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="b5422-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5422-102">SYNOPSIS</span></span>
<span data-ttu-id="b5422-103">Usuwa mapowanie sieci z magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b5422-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="b5422-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5422-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5422-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5422-105">DESCRIPTION</span></span>
<span data-ttu-id="b5422-106">Polecenie cmdlet **Remove-AzureSiteRecoveryNetworkMapping** usuwa mapowanie sieci z bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b5422-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b5422-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5422-107">EXAMPLES</span></span>

### <span data-ttu-id="b5422-108">Przykład 1: Usuwanie mapowania między siecią a siecią odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="b5422-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="b5422-109">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="b5422-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b5422-110">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="b5422-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b5422-111">Drugie polecenie uzyskuje mapowanie między siecią podstawową a siecią odzyskiwania, a następnie zapisuje je w zmiennej $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="b5422-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="b5422-112">Polecenie Określa podstawowy serwer mapowania sieci jako pierwszy element $Servers.</span><span class="sxs-lookup"><span data-stu-id="b5422-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="b5422-113">To polecenie Określa serwer sieci odzyskiwania jako drugi element $Servers.</span><span class="sxs-lookup"><span data-stu-id="b5422-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="b5422-114">Polecenie ostatnie usuwa mapowanie sieci w $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="b5422-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="b5422-115">Przykład 2: Usuwanie mapowania między siecią a siecią maszyny wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b5422-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="b5422-116">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b5422-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="b5422-117">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="b5422-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b5422-118">Drugie polecenie uzyskuje mapowanie między siecią podstawową a siecią maszyny wirtualnej Azure, a następnie zapisuje je w zmiennej $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="b5422-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="b5422-119">Polecenie Określa serwer podstawowy dla sieci jako pierwszy element $Servers.</span><span class="sxs-lookup"><span data-stu-id="b5422-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="b5422-120">Polecenie określa parametr *platformy Azure* .</span><span class="sxs-lookup"><span data-stu-id="b5422-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="b5422-121">Dlatego polecenie uzyskuje mapowanie do sieci maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b5422-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="b5422-122">Polecenie ostatnie usuwa mapowanie sieci w $NetworkMapping.</span><span class="sxs-lookup"><span data-stu-id="b5422-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="b5422-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5422-123">PARAMETERS</span></span>

### <span data-ttu-id="b5422-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b5422-124">-NetworkMapping</span></span>
<span data-ttu-id="b5422-125">Określa mapowanie sieci, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="b5422-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5422-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="b5422-126">-Profile</span></span>
<span data-ttu-id="b5422-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5422-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5422-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b5422-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5422-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5422-129">CommonParameters</span></span>
<span data-ttu-id="b5422-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5422-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5422-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5422-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5422-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5422-132">INPUTS</span></span>

## <span data-ttu-id="b5422-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5422-133">OUTPUTS</span></span>

## <span data-ttu-id="b5422-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5422-134">NOTES</span></span>

## <span data-ttu-id="b5422-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5422-135">RELATED LINKS</span></span>

[<span data-ttu-id="b5422-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b5422-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="b5422-137">Nowe — AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b5422-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="b5422-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b5422-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


