---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527270"
---
# <span data-ttu-id="551e6-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="551e6-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="551e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="551e6-102">SYNOPSIS</span></span>
<span data-ttu-id="551e6-103">Włączanie replikacji elementu do ochrony przez utworzenie elementu chronionego</span><span class="sxs-lookup"><span data-stu-id="551e6-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="551e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="551e6-104">SYNTAX</span></span>

### <span data-ttu-id="551e6-105">DisableD (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="551e6-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551e6-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="551e6-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551e6-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="551e6-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="551e6-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="551e6-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="551e6-109">Opis</span><span class="sxs-lookup"><span data-stu-id="551e6-109">DESCRIPTION</span></span>
<span data-ttu-id="551e6-110">Polecenie cmdlet **New-AzureRmSiteRecoveryReplicationProtectedItem** tworzy nowy element chroniony replikacji.</span><span class="sxs-lookup"><span data-stu-id="551e6-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="551e6-111">Użyj tego polecenia cmdlet, aby włączyć replikację dla elementu chronionego.</span><span class="sxs-lookup"><span data-stu-id="551e6-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="551e6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="551e6-112">EXAMPLES</span></span>

## <span data-ttu-id="551e6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="551e6-113">PARAMETERS</span></span>

### <span data-ttu-id="551e6-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="551e6-114">-Name</span></span>
<span data-ttu-id="551e6-115">Określa nazwę elementu chronionego replikacji za pomocą usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="551e6-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-116">-OS</span><span class="sxs-lookup"><span data-stu-id="551e6-116">-OS</span></span>
<span data-ttu-id="551e6-117">Określa rodzinę systemów operacyjnych.</span><span class="sxs-lookup"><span data-stu-id="551e6-117">Specifies the operating system family.</span></span>
<span data-ttu-id="551e6-118">Dopuszczalne wartości tego parametru to: Windows lub Linux.</span><span class="sxs-lookup"><span data-stu-id="551e6-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="551e6-119">-OSDiskName</span></span>
<span data-ttu-id="551e6-120">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="551e6-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="551e6-121">-ProtectableItem</span></span>
<span data-ttu-id="551e6-122">Określa element ochrona przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="551e6-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="551e6-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="551e6-124">Określa obiekt mapowania kontenera ochrony usługi Azure Site Recovery, który ma być używany do replikacji.</span><span class="sxs-lookup"><span data-stu-id="551e6-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="551e6-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="551e6-126">Określa identyfikator konta usługi Azure Storage, do którego jest replikowana to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="551e6-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="551e6-127">-WaitForCompletion</span></span>
<span data-ttu-id="551e6-128">Wskazuje, że polecenie cmdlet oczekuje na ukończenie.</span><span class="sxs-lookup"><span data-stu-id="551e6-128">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="551e6-129">-Confirm</span></span>
<span data-ttu-id="551e6-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="551e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="551e6-131">-WhatIf</span></span>
<span data-ttu-id="551e6-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="551e6-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="551e6-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="551e6-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551e6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551e6-134">-DefaultProfile</span></span>
<span data-ttu-id="551e6-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="551e6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="551e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551e6-136">CommonParameters</span></span>
<span data-ttu-id="551e6-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551e6-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="551e6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551e6-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="551e6-139">INPUTS</span></span>

### <span data-ttu-id="551e6-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="551e6-140">ASRProtectableItem</span></span>
<span data-ttu-id="551e6-141">Parametr "ProtectableItem" akceptuje wartość typu "ASRProtectableItem" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="551e6-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="551e6-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="551e6-142">OUTPUTS</span></span>

### <span data-ttu-id="551e6-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="551e6-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="551e6-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="551e6-144">NOTES</span></span>

## <span data-ttu-id="551e6-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="551e6-145">RELATED LINKS</span></span>

[<span data-ttu-id="551e6-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="551e6-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="551e6-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="551e6-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="551e6-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="551e6-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
