---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716980"
---
# <span data-ttu-id="89203-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="89203-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="89203-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89203-102">SYNOPSIS</span></span>
<span data-ttu-id="89203-103">Umożliwia ustawienie stanu jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="89203-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89203-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89203-104">SYNTAX</span></span>

### <span data-ttu-id="89203-105">DisableD (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="89203-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89203-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="89203-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89203-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="89203-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89203-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="89203-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89203-109">Opis</span><span class="sxs-lookup"><span data-stu-id="89203-109">DESCRIPTION</span></span>
<span data-ttu-id="89203-110">Polecenie cmdlet **Set-AzureRmSiteRecoveryProtectionEntity** włącza lub wyłącza ochronę jednostki ochrony przed odzyskiwaniem witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="89203-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="89203-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89203-111">EXAMPLES</span></span>

## <span data-ttu-id="89203-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89203-112">PARAMETERS</span></span>

### <span data-ttu-id="89203-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89203-113">-DefaultProfile</span></span>
<span data-ttu-id="89203-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89203-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89203-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89203-115">-Force</span></span>
<span data-ttu-id="89203-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89203-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89203-117">-OS</span><span class="sxs-lookup"><span data-stu-id="89203-117">-OS</span></span>
<span data-ttu-id="89203-118">Określa typ systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="89203-118">Specifies the operating system type.</span></span>
<span data-ttu-id="89203-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89203-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89203-120">Microsoft</span><span class="sxs-lookup"><span data-stu-id="89203-120">Windows</span></span>
- <span data-ttu-id="89203-121">Linux</span><span class="sxs-lookup"><span data-stu-id="89203-121">Linux</span></span>

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

### <span data-ttu-id="89203-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="89203-122">-OSDiskName</span></span>
<span data-ttu-id="89203-123">Określa nazwę dysku zawierającego system operacyjny.</span><span class="sxs-lookup"><span data-stu-id="89203-123">Specifies the name of the disk that contains the operating system.</span></span>

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

### <span data-ttu-id="89203-124">-Policy</span><span class="sxs-lookup"><span data-stu-id="89203-124">-Policy</span></span>
<span data-ttu-id="89203-125">Określa obiekt zasady odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="89203-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89203-126">-Ochrona</span><span class="sxs-lookup"><span data-stu-id="89203-126">-Protection</span></span>
<span data-ttu-id="89203-127">Określa, czy ochrona ma być włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="89203-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="89203-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89203-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89203-129">Włączony</span><span class="sxs-lookup"><span data-stu-id="89203-129">Enable</span></span>
- <span data-ttu-id="89203-130">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="89203-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89203-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="89203-131">-ProtectionEntity</span></span>
<span data-ttu-id="89203-132">Określa obiekt jednostki ochrony.</span><span class="sxs-lookup"><span data-stu-id="89203-132">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89203-133">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="89203-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="89203-134">Określa identyfikator docelowego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="89203-134">Specifies the ID of the target Azure Storage account.</span></span>

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

### <span data-ttu-id="89203-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="89203-135">-WaitForCompletion</span></span>
<span data-ttu-id="89203-136">Wskazuje, że polecenie oczekuje na ukończenie przed zwróceniem.</span><span class="sxs-lookup"><span data-stu-id="89203-136">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="89203-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89203-137">-Confirm</span></span>
<span data-ttu-id="89203-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89203-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89203-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89203-139">-WhatIf</span></span>
<span data-ttu-id="89203-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89203-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="89203-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89203-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89203-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89203-142">CommonParameters</span></span>
<span data-ttu-id="89203-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89203-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89203-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89203-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89203-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89203-145">INPUTS</span></span>

### <span data-ttu-id="89203-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="89203-146">ASRProtectionEntity</span></span>
<span data-ttu-id="89203-147">Parametr "ProtectionEntity" akceptuje wartość typu "ASRProtectionEntity" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="89203-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="89203-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89203-148">OUTPUTS</span></span>

### <span data-ttu-id="89203-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="89203-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="89203-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89203-150">NOTES</span></span>

## <span data-ttu-id="89203-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89203-151">RELATED LINKS</span></span>

[<span data-ttu-id="89203-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="89203-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
