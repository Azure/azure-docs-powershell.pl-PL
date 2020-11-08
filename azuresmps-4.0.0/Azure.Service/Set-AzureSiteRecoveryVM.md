---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054720"
---
# <span data-ttu-id="fd3f3-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="fd3f3-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="fd3f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3f3-103">Ustawia opcje po stronie odzyskiwania dla jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="fd3f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd3f3-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fd3f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="fd3f3-106">Polecenie cmdlet **Set-AzureSiteRecoveryVM** ustawia opcje ochrony po stronie odzyskiwania, takie jak rozmiar maszyny wirtualnej odzyskiwania i sieć maszyny wirtualnej odzyskiwania, dla jednostek ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="fd3f3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="fd3f3-108">Przykład 1: Zezwalanie na aktualizację na chronionej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="fd3f3-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="fd3f3-109">W pierwszym poleceniu jest używane polecenie cmdlet **Get-AzureSiteRecoveryProtectionContainer** w celu uzyskania chronionego kontenera, a następnie zapisanie go w zmiennej $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="fd3f3-110">Drugie polecenie pobiera maszyny wirtualne w $ProtectionContainer, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryVM** , a następnie zapisuje je w zmiennej $VitrualMachines.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="fd3f3-111">Polecenie ostatnie umożliwia aktualizowanie pierwszej maszyny wirtualnej w tablicy $VitrualMachines o nazwie NewVirtualMachine05.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="fd3f3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd3f3-112">PARAMETERS</span></span>

### <span data-ttu-id="fd3f3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd3f3-113">-Name</span></span>
<span data-ttu-id="fd3f3-114">Określa nazwę docelowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-114">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3f3-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="fd3f3-115">-PrimaryNic</span></span>
<span data-ttu-id="fd3f3-116">Określa podstawową kartę sieciową.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-116">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3f3-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="fd3f3-117">-Profile</span></span>
<span data-ttu-id="fd3f3-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd3f3-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd3f3-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="fd3f3-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="fd3f3-121">Określa identyfikator sieci odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3f3-122">-Size</span><span class="sxs-lookup"><span data-stu-id="fd3f3-122">-Size</span></span>
<span data-ttu-id="fd3f3-123">Określa docelowy rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-123">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3f3-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fd3f3-124">-VirtualMachine</span></span>
<span data-ttu-id="fd3f3-125">Określa obiekt maszyny wirtualnej do odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd3f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3f3-126">CommonParameters</span></span>
<span data-ttu-id="fd3f3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd3f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3f3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd3f3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3f3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd3f3-129">INPUTS</span></span>

## <span data-ttu-id="fd3f3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd3f3-130">OUTPUTS</span></span>

## <span data-ttu-id="fd3f3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd3f3-131">NOTES</span></span>

## <span data-ttu-id="fd3f3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd3f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd3f3-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fd3f3-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="fd3f3-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="fd3f3-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


