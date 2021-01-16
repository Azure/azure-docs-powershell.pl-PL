---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358024"
---
# <span data-ttu-id="22393-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="22393-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="22393-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22393-102">SYNOPSIS</span></span>
<span data-ttu-id="22393-103">Tworzy definicję aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="22393-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="22393-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22393-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22393-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22393-105">DESCRIPTION</span></span>
<span data-ttu-id="22393-106">Polecenie cmdlet **New-AzManagedApplicationDefinition** umożliwia utworzenie definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="22393-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="22393-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22393-107">EXAMPLES</span></span>

### <span data-ttu-id="22393-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22393-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="22393-109">To polecenie tworzy definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="22393-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="22393-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22393-110">PARAMETERS</span></span>

### <span data-ttu-id="22393-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22393-111">-ApiVersion</span></span>
<span data-ttu-id="22393-112">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="22393-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="22393-113">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="22393-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="22393-114">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="22393-114">-Authorization</span></span>
<span data-ttu-id="22393-115">Autoryzacja definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="22393-115">The managed application definition authorization.</span></span>
<span data-ttu-id="22393-116">Pary autoryzacji rozdzielanych przecinkami w formacie \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="22393-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="22393-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="22393-117">-CreateUiDefinition</span></span>
<span data-ttu-id="22393-118">Definicja aplikacji zarządzanej Tworzenie definicji interfejsu użytkownika</span><span class="sxs-lookup"><span data-stu-id="22393-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="22393-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22393-119">-DefaultProfile</span></span>
<span data-ttu-id="22393-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22393-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22393-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="22393-121">-Description</span></span>
<span data-ttu-id="22393-122">Opis definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="22393-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="22393-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="22393-123">-DisplayName</span></span>
<span data-ttu-id="22393-124">Nazwa wyświetlana definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="22393-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="22393-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="22393-125">-Location</span></span>
<span data-ttu-id="22393-126">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="22393-126">The resource location.</span></span>

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

### <span data-ttu-id="22393-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="22393-127">-LockLevel</span></span>
<span data-ttu-id="22393-128">Poziom blokady definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="22393-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="22393-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="22393-129">-MainTemplate</span></span>
<span data-ttu-id="22393-130">Szablon główny definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="22393-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="22393-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22393-131">-Name</span></span>
<span data-ttu-id="22393-132">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="22393-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="22393-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="22393-133">-PackageFileUri</span></span>
<span data-ttu-id="22393-134">Identyfikator URI pliku zarządzanego pakietu definicji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="22393-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="22393-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="22393-135">-Pre</span></span>
<span data-ttu-id="22393-136">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="22393-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="22393-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22393-137">-ResourceGroupName</span></span>
<span data-ttu-id="22393-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22393-138">The resource group name.</span></span>

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

### <span data-ttu-id="22393-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="22393-139">-Tag</span></span>
<span data-ttu-id="22393-140">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="22393-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="22393-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22393-141">-Confirm</span></span>
<span data-ttu-id="22393-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22393-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22393-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22393-143">-WhatIf</span></span>
<span data-ttu-id="22393-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22393-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22393-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22393-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22393-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22393-146">CommonParameters</span></span>
<span data-ttu-id="22393-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22393-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22393-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22393-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22393-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22393-149">INPUTS</span></span>

### <span data-ttu-id="22393-150">System. String</span><span class="sxs-lookup"><span data-stu-id="22393-150">System.String</span></span>

### <span data-ttu-id="22393-151">Microsoft. Azure. Commands. resourceName. cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="22393-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="22393-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="22393-152">System.String[]</span></span>

### <span data-ttu-id="22393-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22393-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22393-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22393-154">OUTPUTS</span></span>

### <span data-ttu-id="22393-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="22393-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="22393-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22393-156">NOTES</span></span>

## <span data-ttu-id="22393-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22393-157">RELATED LINKS</span></span>
