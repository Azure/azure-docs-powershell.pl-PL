---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717779"
---
# <span data-ttu-id="6df25-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6df25-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="6df25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6df25-102">SYNOPSIS</span></span>
<span data-ttu-id="6df25-103">Umożliwia ustawienie stanu jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="6df25-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6df25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6df25-104">SYNTAX</span></span>

### <span data-ttu-id="6df25-105">DisableD (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6df25-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6df25-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6df25-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df25-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6df25-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df25-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="6df25-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6df25-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6df25-109">DESCRIPTION</span></span>
<span data-ttu-id="6df25-110">Polecenie cmdlet **Set-AzureRmSiteRecoveryProtectionEntity** włącza lub wyłącza ochronę jednostki ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="6df25-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="6df25-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6df25-111">EXAMPLES</span></span>

## <span data-ttu-id="6df25-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6df25-112">PARAMETERS</span></span>

### <span data-ttu-id="6df25-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6df25-113">-Force</span></span>
<span data-ttu-id="6df25-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6df25-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6df25-115">-OS</span><span class="sxs-lookup"><span data-stu-id="6df25-115">-OS</span></span>
<span data-ttu-id="6df25-116">Określa typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="6df25-116">Specifies the operating system type.</span></span>
<span data-ttu-id="6df25-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6df25-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6df25-118">Microsoft</span><span class="sxs-lookup"><span data-stu-id="6df25-118">Windows</span></span>
- <span data-ttu-id="6df25-119">Linux</span><span class="sxs-lookup"><span data-stu-id="6df25-119">Linux</span></span>

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

### <span data-ttu-id="6df25-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="6df25-120">-OSDiskName</span></span>
<span data-ttu-id="6df25-121">Określa nazwę dysku zawierającego system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="6df25-121">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="6df25-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="6df25-122">-Policy</span></span>
<span data-ttu-id="6df25-123">Określa obiekt zasady odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="6df25-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df25-124">-Ochrona</span><span class="sxs-lookup"><span data-stu-id="6df25-124">-Protection</span></span>
<span data-ttu-id="6df25-125">Określa, czy ochrona ma być włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="6df25-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="6df25-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6df25-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6df25-127">Włączony</span><span class="sxs-lookup"><span data-stu-id="6df25-127">Enable</span></span>
- <span data-ttu-id="6df25-128">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="6df25-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df25-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6df25-129">-ProtectionEntity</span></span>
<span data-ttu-id="6df25-130">Określa obiekt jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="6df25-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6df25-131">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6df25-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6df25-132">Określa identyfikator docelowego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6df25-132">Specifies the ID of the target Azure Storage account.</span></span>

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

### <span data-ttu-id="6df25-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6df25-133">-WaitForCompletion</span></span>
<span data-ttu-id="6df25-134">Wskazuje, że polecenie oczekuje na ukończenie przed zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="6df25-134">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="6df25-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6df25-135">-Confirm</span></span>
<span data-ttu-id="6df25-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6df25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df25-137">-WhatIf</span></span>
<span data-ttu-id="6df25-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6df25-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6df25-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6df25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df25-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df25-140">-DefaultProfile</span></span>
<span data-ttu-id="6df25-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6df25-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6df25-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df25-142">CommonParameters</span></span>
<span data-ttu-id="6df25-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df25-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df25-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df25-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df25-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6df25-145">INPUTS</span></span>

### <span data-ttu-id="6df25-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6df25-146">ASRProtectionEntity</span></span>
<span data-ttu-id="6df25-147">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6df25-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="6df25-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6df25-148">OUTPUTS</span></span>

### <span data-ttu-id="6df25-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6df25-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6df25-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6df25-150">NOTES</span></span>

## <span data-ttu-id="6df25-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6df25-151">RELATED LINKS</span></span>

[<span data-ttu-id="6df25-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="6df25-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
