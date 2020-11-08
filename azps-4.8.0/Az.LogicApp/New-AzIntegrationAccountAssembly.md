---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223446"
---
# <span data-ttu-id="40e71-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="40e71-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="40e71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40e71-102">SYNOPSIS</span></span>
<span data-ttu-id="40e71-103">Tworzy zestaw kont integracyjnych.</span><span class="sxs-lookup"><span data-stu-id="40e71-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="40e71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40e71-104">SYNTAX</span></span>

### <span data-ttu-id="40e71-105">ByIntegrationAccountAndFilePath (domyślny)</span><span class="sxs-lookup"><span data-stu-id="40e71-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e71-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="40e71-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40e71-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="40e71-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40e71-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="40e71-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e71-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="40e71-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e71-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="40e71-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e71-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="40e71-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e71-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="40e71-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e71-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="40e71-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e71-114">Opis</span><span class="sxs-lookup"><span data-stu-id="40e71-114">DESCRIPTION</span></span>
<span data-ttu-id="40e71-115">Polecenie cmdlet **Get-AzIntegrationAccountAssembly** tworzy nowy zestaw na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="40e71-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40e71-116">EXAMPLES</span></span>

### <span data-ttu-id="40e71-117">Przykład 1. Tworzenie nowego zestawu przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="40e71-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="40e71-118">Tworzy nowy zestaw przy użyciu pliku lokalnego znajdującego się w ścieżce pliku znajdującej się w "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="40e71-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="40e71-119">Przykład 2: Tworzenie nowego zestawu przy użyciu bajtów danych</span><span class="sxs-lookup"><span data-stu-id="40e71-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="40e71-120">Tworzy nowy zestaw przy użyciu tablicy bajtowej zawartej w "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="40e71-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="40e71-121">Przykład 3: Tworzenie nowego zestawu za pomocą linku zawartości</span><span class="sxs-lookup"><span data-stu-id="40e71-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="40e71-122">Tworzy nowy zestaw przy użyciu danych bajtowych znajdujących się w adresie URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="40e71-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="40e71-123">Jest to sugerowana metoda tworzenia zestawów o dużym rozmiarze.</span><span class="sxs-lookup"><span data-stu-id="40e71-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="40e71-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40e71-124">PARAMETERS</span></span>

### <span data-ttu-id="40e71-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="40e71-125">-AssemblyData</span></span>
<span data-ttu-id="40e71-126">Dane zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="40e71-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="40e71-127">-AssemblyFilePath</span></span>
<span data-ttu-id="40e71-128">Ścieżka pliku zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="40e71-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="40e71-129">-ContentLink</span></span>
<span data-ttu-id="40e71-130">Publicznie dostępne łącze do danych zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="40e71-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e71-131">-DefaultProfile</span></span>
<span data-ttu-id="40e71-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40e71-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40e71-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="40e71-133">-Metadata</span></span>
<span data-ttu-id="40e71-134">Metadane zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="40e71-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40e71-135">-Name</span></span>
<span data-ttu-id="40e71-136">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="40e71-137">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="40e71-137">-ParentName</span></span>
<span data-ttu-id="40e71-138">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-138">The integration account name.</span></span>

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

### <span data-ttu-id="40e71-139">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="40e71-139">-ParentObject</span></span>
<span data-ttu-id="40e71-140">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-140">An integration account object.</span></span>

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

### <span data-ttu-id="40e71-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="40e71-141">-ParentResourceId</span></span>
<span data-ttu-id="40e71-142">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="40e71-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="40e71-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e71-143">-ResourceGroupName</span></span>
<span data-ttu-id="40e71-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40e71-144">The resource group name.</span></span>

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

### <span data-ttu-id="40e71-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40e71-145">-Confirm</span></span>
<span data-ttu-id="40e71-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e71-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e71-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e71-147">-WhatIf</span></span>
<span data-ttu-id="40e71-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e71-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40e71-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="40e71-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e71-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e71-150">CommonParameters</span></span>
<span data-ttu-id="40e71-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e71-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e71-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e71-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e71-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40e71-153">INPUTS</span></span>

### <span data-ttu-id="40e71-154">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="40e71-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="40e71-155">System. String</span><span class="sxs-lookup"><span data-stu-id="40e71-155">System.String</span></span>

## <span data-ttu-id="40e71-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40e71-156">OUTPUTS</span></span>

### <span data-ttu-id="40e71-157">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="40e71-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="40e71-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40e71-158">NOTES</span></span>

## <span data-ttu-id="40e71-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40e71-159">RELATED LINKS</span></span>
