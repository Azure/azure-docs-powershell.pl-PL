---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4a66541d870d30f2de199297417d211479ecc83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553768"
---
# <span data-ttu-id="1d22b-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="1d22b-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="1d22b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d22b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d22b-103">Tworzy definicję aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d22b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d22b-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d22b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d22b-105">DESCRIPTION</span></span>
<span data-ttu-id="1d22b-106">Polecenie cmdlet **New-AzureRmManagedApplicationDefinition** umożliwia utworzenie definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="1d22b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d22b-107">EXAMPLES</span></span>

### <span data-ttu-id="1d22b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d22b-108">Example 1</span></span>
```
PS C:\> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName "test" -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="1d22b-109">To polecenie tworzy definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="1d22b-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="1d22b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d22b-110">PARAMETERS</span></span>

### <span data-ttu-id="1d22b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1d22b-111">-ApiVersion</span></span>
<span data-ttu-id="1d22b-112">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1d22b-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1d22b-113">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="1d22b-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1d22b-114">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="1d22b-114">-Authorization</span></span>
<span data-ttu-id="1d22b-115">Autoryzacja definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-115">The managed application definition authorization.</span></span>
<span data-ttu-id="1d22b-116">Pary autoryzacji rozdzielanych przecinkami w formacie \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="1d22b-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d22b-117">-DefaultProfile</span></span>
<span data-ttu-id="1d22b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d22b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d22b-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="1d22b-119">-Description</span></span>
<span data-ttu-id="1d22b-120">Opis definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-120">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1d22b-121">-DisplayName</span></span>
<span data-ttu-id="1d22b-122">Nazwa wyświetlana definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-122">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1d22b-123">-Location</span></span>
<span data-ttu-id="1d22b-124">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1d22b-124">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-125">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="1d22b-125">-LockLevel</span></span>
<span data-ttu-id="1d22b-126">Poziom blokady definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-126">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d22b-127">-Name</span></span>
<span data-ttu-id="1d22b-128">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-128">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-129">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="1d22b-129">-PackageFileUri</span></span>
<span data-ttu-id="1d22b-130">Identyfikator URI pliku zarządzanego pakietu definicji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1d22b-130">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="1d22b-131">-Pre</span></span>
<span data-ttu-id="1d22b-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="1d22b-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1d22b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d22b-133">-ResourceGroupName</span></span>
<span data-ttu-id="1d22b-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1d22b-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d22b-135">-Tag</span></span>
<span data-ttu-id="1d22b-136">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="1d22b-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d22b-137">-Confirm</span></span>
<span data-ttu-id="1d22b-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d22b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d22b-139">-WhatIf</span></span>
<span data-ttu-id="1d22b-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d22b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d22b-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d22b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-142">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="1d22b-142">-CreateUiDefinition</span></span>
<span data-ttu-id="1d22b-143">Definicja aplikacji zarządzanej Utwórz definicję interfejsu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1d22b-143">The managed application definition create ui definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-144">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="1d22b-144">-MainTemplate</span></span>
<span data-ttu-id="1d22b-145">Szablon główny definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="1d22b-145">The managed application definition main template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d22b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d22b-146">CommonParameters</span></span>
<span data-ttu-id="1d22b-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d22b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d22b-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d22b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d22b-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d22b-149">INPUTS</span></span>

### <span data-ttu-id="1d22b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1d22b-150">System.String</span></span>
<span data-ttu-id="1d22b-151">Microsoft. Azure. Commands. resourceName. cmdlets. Entities. Application. ApplicationLockLevel system. String [] system. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1d22b-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="1d22b-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d22b-152">OUTPUTS</span></span>

### <span data-ttu-id="1d22b-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1d22b-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1d22b-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d22b-154">NOTES</span></span>

## <span data-ttu-id="1d22b-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d22b-155">RELATED LINKS</span></span>

