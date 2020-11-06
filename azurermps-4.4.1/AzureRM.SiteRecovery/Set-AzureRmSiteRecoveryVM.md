---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 483D4C1A-D34E-40ED-B92B-82187FF321F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 7cfc764e5c9c3c5bb11290220cc04b2baa781070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549831"
---
# <span data-ttu-id="0b297-101">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="0b297-101">Set-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="0b297-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b297-102">SYNOPSIS</span></span>
<span data-ttu-id="0b297-103">Ustawia opcje po stronie odzyskiwania dla jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="0b297-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b297-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b297-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-RecoveryNicSubnetName <String>]
 [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b297-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b297-105">DESCRIPTION</span></span>
<span data-ttu-id="0b297-106">Polecenie cmdlet **Set-AzureRmSiteRecoveryVM** ustawia opcje ochrony po stronie odzyskiwania, takie jak rozmiar maszyny wirtualnej odzyskiwania i sieć maszyny wirtualnej odzyskiwania, dla jednostek ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0b297-106">The **Set-AzureRmSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="0b297-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b297-107">EXAMPLES</span></span>

## <span data-ttu-id="0b297-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b297-108">PARAMETERS</span></span>

### <span data-ttu-id="0b297-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b297-109">-Name</span></span>
<span data-ttu-id="0b297-110">Określa nazwę docelowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b297-110">Specifies the name of the target virtual machine.</span></span>

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

### <span data-ttu-id="0b297-111">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="0b297-111">-NicSelectionType</span></span>
<span data-ttu-id="0b297-112">Określa właściwości wyboru karty sieciowej.</span><span class="sxs-lookup"><span data-stu-id="0b297-112">Specifies the network adapter selection properties.</span></span>
<span data-ttu-id="0b297-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0b297-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b297-114">NotSelected</span><span class="sxs-lookup"><span data-stu-id="0b297-114">NotSelected</span></span>
- <span data-ttu-id="0b297-115">SelectedByUser</span><span class="sxs-lookup"><span data-stu-id="0b297-115">SelectedByUser</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b297-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="0b297-116">-PrimaryNic</span></span>
<span data-ttu-id="0b297-117">Określa podstawową kartę sieciową.</span><span class="sxs-lookup"><span data-stu-id="0b297-117">Specifies the primary network adapter card.</span></span>

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

### <span data-ttu-id="0b297-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="0b297-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="0b297-119">Określa identyfikator sieci odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0b297-119">Specifies the recovery network ID.</span></span>

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

### <span data-ttu-id="0b297-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="0b297-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="0b297-121">Określa statyczny adres IP, który jest przypisany głównemu kontrolerowi karty sieciowej podczas odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0b297-121">Specifies the static IP address that is assigned to primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="0b297-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="0b297-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="0b297-123">Określa nazwę podsieci sieci wirtualnej platformy Azure, z którą jest dołączany podstawowy kontroler karty sieciowej podczas odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0b297-123">Specifies the Azure virtual network subnet name with which to attach the primary network adapter controller on recovery.</span></span>

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

### <span data-ttu-id="0b297-124">-Size</span><span class="sxs-lookup"><span data-stu-id="0b297-124">-Size</span></span>
<span data-ttu-id="0b297-125">Określa docelowy rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0b297-125">Specifies the target virtual machine size.</span></span>

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

### <span data-ttu-id="0b297-126">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0b297-126">-VirtualMachine</span></span>
<span data-ttu-id="0b297-127">Określa obiekt maszyny wirtualnej do odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="0b297-127">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b297-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b297-128">-DefaultProfile</span></span>
<span data-ttu-id="0b297-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b297-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b297-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b297-130">CommonParameters</span></span>
<span data-ttu-id="0b297-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b297-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b297-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b297-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b297-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b297-133">INPUTS</span></span>

### <span data-ttu-id="0b297-134">ASRVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0b297-134">ASRVirtualMachine</span></span>
<span data-ttu-id="0b297-135">Parametr "VirtualMachine" akceptuje wartość typu "ASRVirtualMachine" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0b297-135">Parameter 'VirtualMachine' accepts value of type 'ASRVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="0b297-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b297-136">OUTPUTS</span></span>

### <span data-ttu-id="0b297-137">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0b297-137">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0b297-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b297-138">NOTES</span></span>

## <span data-ttu-id="0b297-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b297-139">RELATED LINKS</span></span>

[<span data-ttu-id="0b297-140">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="0b297-140">Get-AzureRmSiteRecoveryVM</span></span>](./Get-AzureRmSiteRecoveryVM.md)
