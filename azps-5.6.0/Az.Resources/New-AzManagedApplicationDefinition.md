---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 947cd0674e5fcd704b305b5963f3ed06e008f3fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971802"
---
# <span data-ttu-id="e6046-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="e6046-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="e6046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6046-102">SYNOPSIS</span></span>
<span data-ttu-id="e6046-103">Tworzy zarządzaną definicję aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6046-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="e6046-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6046-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6046-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6046-105">DESCRIPTION</span></span>
<span data-ttu-id="e6046-106">Polecenie **cmdlet New-AzManagedApplicationDefinition** tworzy definicję aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e6046-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="e6046-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6046-107">EXAMPLES</span></span>

### <span data-ttu-id="e6046-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6046-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="e6046-109">To polecenie tworzy zarządzaną definicję aplikacji</span><span class="sxs-lookup"><span data-stu-id="e6046-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="e6046-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6046-110">PARAMETERS</span></span>

### <span data-ttu-id="e6046-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e6046-111">-ApiVersion</span></span>
<span data-ttu-id="e6046-112">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="e6046-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e6046-113">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="e6046-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e6046-114">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="e6046-114">-Authorization</span></span>
<span data-ttu-id="e6046-115">Autoryzacja definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e6046-115">The managed application definition authorization.</span></span>
<span data-ttu-id="e6046-116">Pary autoryzacji oddzielone przecinkami w \<principalId\> formacie:\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="e6046-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="e6046-117">- CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="e6046-117">-CreateUiDefinition</span></span>
<span data-ttu-id="e6046-118">Definicja aplikacji zarządzanej utwórz definicję interfejsu użytkownika</span><span class="sxs-lookup"><span data-stu-id="e6046-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="e6046-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6046-119">-DefaultProfile</span></span>
<span data-ttu-id="e6046-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6046-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6046-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="e6046-121">-Description</span></span>
<span data-ttu-id="e6046-122">Opis definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e6046-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="e6046-123">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="e6046-123">-DisplayName</span></span>
<span data-ttu-id="e6046-124">Nazwa wyświetlana definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e6046-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="e6046-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e6046-125">-Location</span></span>
<span data-ttu-id="e6046-126">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e6046-126">The resource location.</span></span>

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

### <span data-ttu-id="e6046-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="e6046-127">-LockLevel</span></span>
<span data-ttu-id="e6046-128">Poziom blokady dla definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e6046-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="e6046-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="e6046-129">-MainTemplate</span></span>
<span data-ttu-id="e6046-130">Główny szablon definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="e6046-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="e6046-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6046-131">-Name</span></span>
<span data-ttu-id="e6046-132">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e6046-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="e6046-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="e6046-133">-PackageFileUri</span></span>
<span data-ttu-id="e6046-134">Uri pliku pakietu definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e6046-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="e6046-135">— Przed</span><span class="sxs-lookup"><span data-stu-id="e6046-135">-Pre</span></span>
<span data-ttu-id="e6046-136">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e6046-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e6046-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6046-137">-ResourceGroupName</span></span>
<span data-ttu-id="e6046-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6046-138">The resource group name.</span></span>

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

### <span data-ttu-id="e6046-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="e6046-139">-Tag</span></span>
<span data-ttu-id="e6046-140">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6046-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e6046-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6046-141">-Confirm</span></span>
<span data-ttu-id="e6046-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6046-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6046-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6046-143">-WhatIf</span></span>
<span data-ttu-id="e6046-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6046-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6046-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6046-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6046-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6046-146">CommonParameters</span></span>
<span data-ttu-id="e6046-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6046-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6046-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6046-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6046-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6046-149">INPUTS</span></span>

### <span data-ttu-id="e6046-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e6046-150">System.String</span></span>

### <span data-ttu-id="e6046-151">Microsoft.Azure.Commands.ResourceManager.Cmdlet.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="e6046-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="e6046-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e6046-152">System.String[]</span></span>

### <span data-ttu-id="e6046-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6046-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e6046-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6046-154">OUTPUTS</span></span>

### <span data-ttu-id="e6046-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e6046-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e6046-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6046-156">NOTES</span></span>

## <span data-ttu-id="e6046-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6046-157">RELATED LINKS</span></span>
