---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 28b2f976b85d7db40cdb80cf2b9b58a2d7692952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551523"
---
# <span data-ttu-id="37267-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="37267-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="37267-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37267-102">SYNOPSIS</span></span>
<span data-ttu-id="37267-103">Włączanie replikacji elementu do ochrony przez utworzenie elementu chronionego</span><span class="sxs-lookup"><span data-stu-id="37267-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37267-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37267-104">SYNTAX</span></span>

### <span data-ttu-id="37267-105">DisableD (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="37267-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37267-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="37267-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37267-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="37267-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37267-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="37267-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37267-109">Opis</span><span class="sxs-lookup"><span data-stu-id="37267-109">DESCRIPTION</span></span>
<span data-ttu-id="37267-110">Polecenie cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** tworzy nowy element chroniony replikacji.</span><span class="sxs-lookup"><span data-stu-id="37267-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="37267-111">Użyj tego polecenia cmdlet, aby włączyć replikację dla elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="37267-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="37267-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37267-112">EXAMPLES</span></span>

## <span data-ttu-id="37267-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37267-113">PARAMETERS</span></span>

### <span data-ttu-id="37267-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37267-114">-DefaultProfile</span></span>
<span data-ttu-id="37267-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37267-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37267-116">-Name</span></span>
<span data-ttu-id="37267-117">Określa nazwę elementu chronionego replikacji za pomocą usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="37267-117">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-118">-OS</span><span class="sxs-lookup"><span data-stu-id="37267-118">-OS</span></span>
<span data-ttu-id="37267-119">Określa rodzinę systemów operacyjnych.</span><span class="sxs-lookup"><span data-stu-id="37267-119">Specifies the operating system family.</span></span>
<span data-ttu-id="37267-120">Dopuszczalne wartości tego parametru to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="37267-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="37267-121">-OSDiskName</span></span>
<span data-ttu-id="37267-122">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="37267-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="37267-123">-ProtectableItem</span></span>
<span data-ttu-id="37267-124">Określa element ochrona przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="37267-124">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37267-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="37267-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="37267-126">Określa obiekt mapowania kontenera ochrony usługi Azure Site Recovery, który ma być używany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="37267-126">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="37267-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="37267-128">Określa identyfikator konta usługi Azure Storage, do którego jest replikowana to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37267-128">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-129">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="37267-129">-WaitForCompletion</span></span>
<span data-ttu-id="37267-130">Wskazuje, że polecenie cmdlet oczekuje na ukończenie.</span><span class="sxs-lookup"><span data-stu-id="37267-130">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37267-131">-Confirm</span></span>
<span data-ttu-id="37267-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37267-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37267-133">-WhatIf</span></span>
<span data-ttu-id="37267-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37267-134">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="37267-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37267-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37267-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37267-136">CommonParameters</span></span>
<span data-ttu-id="37267-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37267-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37267-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37267-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37267-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37267-139">INPUTS</span></span>

### <span data-ttu-id="37267-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="37267-140">ASRProtectableItem</span></span>
<span data-ttu-id="37267-141">Parametr "ProtectableItem" akceptuje wartość typu "ASRProtectableItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="37267-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="37267-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37267-142">OUTPUTS</span></span>

### <span data-ttu-id="37267-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="37267-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="37267-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37267-144">NOTES</span></span>

## <span data-ttu-id="37267-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37267-145">RELATED LINKS</span></span>

[<span data-ttu-id="37267-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="37267-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="37267-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="37267-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="37267-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="37267-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
