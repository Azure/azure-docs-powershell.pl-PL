---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542892"
---
# <span data-ttu-id="7b24b-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b24b-101">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="7b24b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b24b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b24b-103">Ustawia właściwości odzyskiwania, takie jak Sieć docelowa i rozmiar maszyny wirtualnej dla elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="7b24b-103">Sets recovery properties such as target network and virtual machine size for a Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b24b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b24b-104">SYNTAX</span></span>

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b24b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b24b-105">DESCRIPTION</span></span>
<span data-ttu-id="7b24b-106">Polecenie cmdlet **Set-AzureRmSiteRecoveryReplicationProtectedItem** ustawia właściwości odzyskiwania elementu chronionego replikacji.</span><span class="sxs-lookup"><span data-stu-id="7b24b-106">The **Set-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="7b24b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b24b-107">EXAMPLES</span></span>

## <span data-ttu-id="7b24b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b24b-108">PARAMETERS</span></span>

### <span data-ttu-id="7b24b-109">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7b24b-109">-LicenseType</span></span>
<span data-ttu-id="7b24b-110">Określa wybór typu licencji dla maszyn wirtualnych systemu Windows Server migrowanych za pośrednictwem usługi hybrydowego użytkowania.</span><span class="sxs-lookup"><span data-stu-id="7b24b-110">Specifies the license type selection for Windows Server virtual machines migrated through Hybrid use benefit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b24b-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b24b-111">-Name</span></span>
<span data-ttu-id="7b24b-112">Określa nazwę maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7b24b-112">Specifies the name of the recovery virtual machine.</span></span>

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

### <span data-ttu-id="7b24b-113">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="7b24b-113">-NicSelectionType</span></span>
<span data-ttu-id="7b24b-114">Określa właściwości karty interfejsu sieciowego (NIC), które są ustawiane przez użytkownika lub ustawione domyślnie.</span><span class="sxs-lookup"><span data-stu-id="7b24b-114">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="7b24b-115">Możesz określić NotSelected, aby wrócić do wartości domyślnych.</span><span class="sxs-lookup"><span data-stu-id="7b24b-115">You can specify NotSelected to go back to the default values.</span></span>

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

### <span data-ttu-id="7b24b-116">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="7b24b-116">-PrimaryNic</span></span>
<span data-ttu-id="7b24b-117">Określa kartę sieciową maszyny wirtualnej, dla której to polecenie cmdlet ustawia właściwość sieć odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7b24b-117">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="7b24b-118">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="7b24b-118">-RecoveryNetworkId</span></span>
<span data-ttu-id="7b24b-119">Określa identyfikator sieci wirtualnej platformy Azure, dla którego to polecenie cmdlet odsłuży do odkrycia chronionego elementu.</span><span class="sxs-lookup"><span data-stu-id="7b24b-119">Specifies the ID of the Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="7b24b-120">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="7b24b-120">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="7b24b-121">Określa statyczny adres IP, który powinien być przypisany do podstawowej karty sieciowej przy odzyskiwaniu.</span><span class="sxs-lookup"><span data-stu-id="7b24b-121">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="7b24b-122">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="7b24b-122">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="7b24b-123">Określa nazwę podsieci w wirtualnej sieci Azure odzyskiwania, dla której ten polecenie cmdlet odzyskuje chroniony element.</span><span class="sxs-lookup"><span data-stu-id="7b24b-123">Specifies the name of the Subnet on the recovery Azure virtual network for which this cmdlet recovers the Protected Item.</span></span>

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

### <span data-ttu-id="7b24b-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b24b-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7b24b-125">Określa element chroniony replikacji odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="7b24b-125">Specifies the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b24b-126">-Size</span><span class="sxs-lookup"><span data-stu-id="7b24b-126">-Size</span></span>
<span data-ttu-id="7b24b-127">Określa rozmiar maszyny wirtualnej odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7b24b-127">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="7b24b-128">Wartość powinna pochodzić z zestawu rozmiarów obsługiwanych przez maszyny wirtualne platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7b24b-128">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="7b24b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b24b-129">-DefaultProfile</span></span>
<span data-ttu-id="7b24b-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b24b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b24b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b24b-131">CommonParameters</span></span>
<span data-ttu-id="7b24b-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b24b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b24b-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b24b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b24b-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b24b-134">INPUTS</span></span>

### <span data-ttu-id="7b24b-135">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b24b-135">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="7b24b-136">Parametr "ReplicationProtectedItem" akceptuje wartość typu "ASRReplicationProtectedItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="7b24b-136">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="7b24b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b24b-137">OUTPUTS</span></span>

### <span data-ttu-id="7b24b-138">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7b24b-138">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7b24b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b24b-139">NOTES</span></span>

## <span data-ttu-id="7b24b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b24b-140">RELATED LINKS</span></span>

[<span data-ttu-id="7b24b-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b24b-141">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="7b24b-142">Nowe — AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b24b-142">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="7b24b-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7b24b-143">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
