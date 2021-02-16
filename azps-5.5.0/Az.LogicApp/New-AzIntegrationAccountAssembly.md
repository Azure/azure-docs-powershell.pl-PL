---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180363"
---
# <span data-ttu-id="e2c52-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e2c52-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="e2c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2c52-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c52-103">Tworzy zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="e2c52-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2c52-104">SYNTAX</span></span>

### <span data-ttu-id="e2c52-105">ByIntegrationAccountAndFilePath (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e2c52-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c52-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e2c52-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2c52-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e2c52-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2c52-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e2c52-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c52-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e2c52-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c52-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e2c52-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c52-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e2c52-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c52-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e2c52-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2c52-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e2c52-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2c52-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2c52-114">DESCRIPTION</span></span>
<span data-ttu-id="e2c52-115">Polecenie **cmdlet Get-AzIntegrationAccountAssembly** tworzy nowy zestaw na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="e2c52-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2c52-116">EXAMPLES</span></span>

### <span data-ttu-id="e2c52-117">Przykład 1. Tworzenie nowego zestawu przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="e2c52-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e2c52-118">Tworzy nowy zestaw przy użyciu pliku lokalnego znajdującego się w ścieżce pliku zawartej w pliku "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="e2c52-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="e2c52-119">Przykład 2. Tworzenie nowego zestawu przy użyciu danych bajtowych</span><span class="sxs-lookup"><span data-stu-id="e2c52-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e2c52-120">Tworzy nowy zestaw przy użyciu tablicy bajtów zawartej w "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="e2c52-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="e2c52-121">Przykład 3. Tworzenie nowego zestawu przy użyciu linku zawartości</span><span class="sxs-lookup"><span data-stu-id="e2c52-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e2c52-122">Tworzy nowy zestaw przy użyciu danych bajtowych znajdujących się w adresie URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="e2c52-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="e2c52-123">Jest to sugerowana metoda tworzenia dużych zestawów.</span><span class="sxs-lookup"><span data-stu-id="e2c52-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="e2c52-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2c52-124">PARAMETERS</span></span>

### <span data-ttu-id="e2c52-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="e2c52-125">-AssemblyData</span></span>
<span data-ttu-id="e2c52-126">Dane bajtowe zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="e2c52-127">-AssemblyFilePath</span></span>
<span data-ttu-id="e2c52-128">Ścieżka pliku zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-129">- ContentLink</span><span class="sxs-lookup"><span data-stu-id="e2c52-129">-ContentLink</span></span>
<span data-ttu-id="e2c52-130">Publicznie dostępny link do danych zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c52-131">-DefaultProfile</span></span>
<span data-ttu-id="e2c52-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2c52-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2c52-133">— Metadane</span><span class="sxs-lookup"><span data-stu-id="e2c52-133">-Metadata</span></span>
<span data-ttu-id="e2c52-134">Metadane zestawu kont integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e2c52-135">-Name</span></span>
<span data-ttu-id="e2c52-136">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e2c52-137">-ParentName</span></span>
<span data-ttu-id="e2c52-138">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-139">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="e2c52-139">-ParentObject</span></span>
<span data-ttu-id="e2c52-140">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e2c52-141">-ParentResourceId</span></span>
<span data-ttu-id="e2c52-142">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="e2c52-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2c52-143">-ResourceGroupName</span></span>
<span data-ttu-id="e2c52-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2c52-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2c52-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2c52-145">-Confirm</span></span>
<span data-ttu-id="e2c52-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e2c52-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2c52-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2c52-147">-WhatIf</span></span>
<span data-ttu-id="e2c52-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2c52-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2c52-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e2c52-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2c52-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c52-150">CommonParameters</span></span>
<span data-ttu-id="e2c52-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c52-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c52-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c52-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c52-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2c52-153">INPUTS</span></span>

### <span data-ttu-id="e2c52-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e2c52-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="e2c52-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e2c52-155">System.String</span></span>

## <span data-ttu-id="e2c52-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2c52-156">OUTPUTS</span></span>

### <span data-ttu-id="e2c52-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e2c52-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="e2c52-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2c52-158">NOTES</span></span>

## <span data-ttu-id="e2c52-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2c52-159">RELATED LINKS</span></span>
