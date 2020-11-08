---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049402"
---
# <span data-ttu-id="350da-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="350da-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="350da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="350da-102">SYNOPSIS</span></span>
<span data-ttu-id="350da-103">Modyfikuje zestaw kont integracyjnych.</span><span class="sxs-lookup"><span data-stu-id="350da-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="350da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="350da-104">SYNTAX</span></span>

### <span data-ttu-id="350da-105">ByIntegrationAccountAndFilePath (domyślny)</span><span class="sxs-lookup"><span data-stu-id="350da-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350da-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="350da-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="350da-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="350da-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="350da-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="350da-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350da-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="350da-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350da-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="350da-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350da-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="350da-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350da-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="350da-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="350da-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="350da-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="350da-114">Opis</span><span class="sxs-lookup"><span data-stu-id="350da-114">DESCRIPTION</span></span>
<span data-ttu-id="350da-115">Polecenie cmdlet **Set-AzIntegrationAccountAssembly** modyfikuje zestaw kont integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="350da-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="350da-116">EXAMPLES</span></span>

### <span data-ttu-id="350da-117">Przykład 1: modyfikowanie zestawu przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="350da-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="350da-118">Modyfikuje zestaw o nazwie "sampleAssembly" przy użyciu pliku lokalnego znajdującego się w ścieżce pliku znajdującej się w "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="350da-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="350da-119">Przykład 2: modyfikowanie zestawu za pomocą bajtów danych</span><span class="sxs-lookup"><span data-stu-id="350da-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="350da-120">Modyfikuje zestaw o nazwie "sampleAssembly" przy użyciu tablicy bajtowej zawartej w "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="350da-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="350da-121">Przykład 3: modyfikowanie zestawu za pomocą linku do zawartości</span><span class="sxs-lookup"><span data-stu-id="350da-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="350da-122">Modyfikuje zestaw o nazwie "sampleAssembly" przy użyciu danych bajtowych znajdujących się w adresie URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="350da-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="350da-123">Jest to sugerowana metoda tworzenia zestawów o dużym rozmiarze.</span><span class="sxs-lookup"><span data-stu-id="350da-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="350da-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="350da-124">PARAMETERS</span></span>

### <span data-ttu-id="350da-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="350da-125">-AssemblyData</span></span>
<span data-ttu-id="350da-126">Dane zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="350da-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="350da-127">-AssemblyFilePath</span></span>
<span data-ttu-id="350da-128">Ścieżka pliku zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="350da-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="350da-129">-ContentLink</span></span>
<span data-ttu-id="350da-130">Publicznie dostępne łącze do danych zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="350da-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="350da-131">-DefaultProfile</span></span>
<span data-ttu-id="350da-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="350da-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="350da-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="350da-133">-InputObject</span></span>
<span data-ttu-id="350da-134">Zestaw kont integracyjnych.</span><span class="sxs-lookup"><span data-stu-id="350da-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="350da-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="350da-135">-Metadata</span></span>
<span data-ttu-id="350da-136">Metadane zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="350da-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="350da-137">-Name</span></span>
<span data-ttu-id="350da-138">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="350da-139">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="350da-139">-ParentName</span></span>
<span data-ttu-id="350da-140">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-140">The integration account name.</span></span>

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

### <span data-ttu-id="350da-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="350da-141">-ResourceGroupName</span></span>
<span data-ttu-id="350da-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="350da-142">The resource group name.</span></span>

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

### <span data-ttu-id="350da-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="350da-143">-ResourceId</span></span>
<span data-ttu-id="350da-144">Identyfikator zasobu zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="350da-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="350da-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="350da-145">-Confirm</span></span>
<span data-ttu-id="350da-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350da-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="350da-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="350da-147">-WhatIf</span></span>
<span data-ttu-id="350da-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350da-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="350da-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="350da-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="350da-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350da-150">CommonParameters</span></span>
<span data-ttu-id="350da-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350da-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350da-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="350da-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350da-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="350da-153">INPUTS</span></span>

### <span data-ttu-id="350da-154">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="350da-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="350da-155">System. String</span><span class="sxs-lookup"><span data-stu-id="350da-155">System.String</span></span>

## <span data-ttu-id="350da-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="350da-156">OUTPUTS</span></span>

### <span data-ttu-id="350da-157">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="350da-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="350da-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="350da-158">NOTES</span></span>

## <span data-ttu-id="350da-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="350da-159">RELATED LINKS</span></span>
