---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 74531aa3c5e142cf3c9638f4910c8d45654a20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987834"
---
# <span data-ttu-id="90819-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="90819-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="90819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90819-102">SYNOPSIS</span></span>
<span data-ttu-id="90819-103">Modyfikuje zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="90819-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="90819-104">SYNTAX</span></span>

### <span data-ttu-id="90819-105">ByIntegrationAccountAndFilePath (domyślne)</span><span class="sxs-lookup"><span data-stu-id="90819-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90819-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="90819-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90819-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="90819-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90819-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="90819-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90819-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="90819-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90819-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="90819-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90819-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="90819-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90819-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="90819-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90819-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="90819-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90819-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="90819-114">DESCRIPTION</span></span>
<span data-ttu-id="90819-115">Polecenie **cmdlet Set-AzIntegrationAccountAssembly** modyfikuje zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="90819-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="90819-116">EXAMPLES</span></span>

### <span data-ttu-id="90819-117">Przykład 1. Modyfikowanie zestawu przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="90819-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="90819-118">Modyfikuje zestaw o nazwie "sampleAssembly" przy użyciu pliku lokalnego znajdującego się w ścieżce pliku zawartej w pliku "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="90819-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="90819-119">Przykład 2. Modyfikowanie zestawu przy użyciu danych bajtowych</span><span class="sxs-lookup"><span data-stu-id="90819-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="90819-120">Modyfikuje zestaw o nazwie "sampleAssembly" przy użyciu tablicy bajtowej zawartej w "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="90819-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="90819-121">Przykład 3. Modyfikowanie zestawu przy użyciu linku zawartości</span><span class="sxs-lookup"><span data-stu-id="90819-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="90819-122">Modyfikuje zestaw o nazwie "sampleAssembly" przy użyciu danych bajtowych znajdujących się w adresie URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="90819-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="90819-123">Jest to sugerowana metoda tworzenia zespołów o dużych rozmiarach.</span><span class="sxs-lookup"><span data-stu-id="90819-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="90819-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90819-124">PARAMETERS</span></span>

### <span data-ttu-id="90819-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="90819-125">-AssemblyData</span></span>
<span data-ttu-id="90819-126">Dane bajtowe zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="90819-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="90819-127">-AssemblyFilePath</span></span>
<span data-ttu-id="90819-128">Ścieżka pliku zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="90819-129">— ContentLink</span><span class="sxs-lookup"><span data-stu-id="90819-129">-ContentLink</span></span>
<span data-ttu-id="90819-130">Publicznie dostępny link do danych zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="90819-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90819-131">-DefaultProfile</span></span>
<span data-ttu-id="90819-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="90819-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90819-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90819-133">-InputObject</span></span>
<span data-ttu-id="90819-134">Zestaw konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90819-135">— Metadane</span><span class="sxs-lookup"><span data-stu-id="90819-135">-Metadata</span></span>
<span data-ttu-id="90819-136">Metadane zestawu kont integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="90819-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="90819-137">-Name</span></span>
<span data-ttu-id="90819-138">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90819-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="90819-139">-ParentName</span></span>
<span data-ttu-id="90819-140">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-140">The integration account name.</span></span>

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

### <span data-ttu-id="90819-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90819-141">-ResourceGroupName</span></span>
<span data-ttu-id="90819-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90819-142">The resource group name.</span></span>

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

### <span data-ttu-id="90819-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90819-143">-ResourceId</span></span>
<span data-ttu-id="90819-144">Identyfikator zasobu zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="90819-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="90819-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90819-145">-Confirm</span></span>
<span data-ttu-id="90819-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90819-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90819-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90819-147">-WhatIf</span></span>
<span data-ttu-id="90819-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90819-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90819-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="90819-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90819-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90819-150">CommonParameters</span></span>
<span data-ttu-id="90819-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90819-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90819-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90819-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90819-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90819-153">INPUTS</span></span>

### <span data-ttu-id="90819-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="90819-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="90819-155">System.String</span><span class="sxs-lookup"><span data-stu-id="90819-155">System.String</span></span>

## <span data-ttu-id="90819-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90819-156">OUTPUTS</span></span>

### <span data-ttu-id="90819-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="90819-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="90819-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="90819-158">NOTES</span></span>

## <span data-ttu-id="90819-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90819-159">RELATED LINKS</span></span>
