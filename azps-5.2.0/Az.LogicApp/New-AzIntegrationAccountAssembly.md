---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324170"
---
# <span data-ttu-id="de06a-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="de06a-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="de06a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de06a-102">SYNOPSIS</span></span>
<span data-ttu-id="de06a-103">Tworzy zestaw kont integracyjnych.</span><span class="sxs-lookup"><span data-stu-id="de06a-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="de06a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de06a-104">SYNTAX</span></span>

### <span data-ttu-id="de06a-105">ByIntegrationAccountAndFilePath (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de06a-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de06a-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="de06a-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de06a-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="de06a-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de06a-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="de06a-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de06a-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="de06a-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de06a-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="de06a-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de06a-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="de06a-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de06a-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="de06a-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de06a-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="de06a-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de06a-114">Opis</span><span class="sxs-lookup"><span data-stu-id="de06a-114">DESCRIPTION</span></span>
<span data-ttu-id="de06a-115">Polecenie cmdlet **Get-AzIntegrationAccountAssembly** tworzy nowy zestaw na koncie integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="de06a-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de06a-116">EXAMPLES</span></span>

### <span data-ttu-id="de06a-117">Przykład 1. Tworzenie nowego zestawu przy użyciu pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="de06a-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="de06a-118">Tworzy nowy zestaw przy użyciu pliku lokalnego znajdującego się w ścieżce pliku znajdującej się w "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="de06a-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="de06a-119">Przykład 2: Tworzenie nowego zestawu przy użyciu bajtów danych</span><span class="sxs-lookup"><span data-stu-id="de06a-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="de06a-120">Tworzy nowy zestaw przy użyciu tablicy bajtowej zawartej w "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="de06a-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="de06a-121">Przykład 3: Tworzenie nowego zestawu za pomocą linku zawartości</span><span class="sxs-lookup"><span data-stu-id="de06a-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="de06a-122">Tworzy nowy zestaw przy użyciu danych bajtowych znajdujących się w adresie URL "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="de06a-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="de06a-123">Jest to sugerowana metoda tworzenia zestawów o dużym rozmiarze.</span><span class="sxs-lookup"><span data-stu-id="de06a-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="de06a-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de06a-124">PARAMETERS</span></span>

### <span data-ttu-id="de06a-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="de06a-125">-AssemblyData</span></span>
<span data-ttu-id="de06a-126">Dane zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="de06a-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="de06a-127">-AssemblyFilePath</span></span>
<span data-ttu-id="de06a-128">Ścieżka pliku zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="de06a-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="de06a-129">-ContentLink</span></span>
<span data-ttu-id="de06a-130">Publicznie dostępne łącze do danych zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="de06a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de06a-131">-DefaultProfile</span></span>
<span data-ttu-id="de06a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de06a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de06a-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="de06a-133">-Metadata</span></span>
<span data-ttu-id="de06a-134">Metadane zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="de06a-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de06a-135">-Name</span></span>
<span data-ttu-id="de06a-136">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="de06a-137">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="de06a-137">-ParentName</span></span>
<span data-ttu-id="de06a-138">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-138">The integration account name.</span></span>

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

### <span data-ttu-id="de06a-139">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="de06a-139">-ParentObject</span></span>
<span data-ttu-id="de06a-140">Obiekt konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-140">An integration account object.</span></span>

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

### <span data-ttu-id="de06a-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="de06a-141">-ParentResourceId</span></span>
<span data-ttu-id="de06a-142">Identyfikator zasobu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="de06a-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="de06a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de06a-143">-ResourceGroupName</span></span>
<span data-ttu-id="de06a-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de06a-144">The resource group name.</span></span>

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

### <span data-ttu-id="de06a-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de06a-145">-Confirm</span></span>
<span data-ttu-id="de06a-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de06a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de06a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de06a-147">-WhatIf</span></span>
<span data-ttu-id="de06a-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de06a-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de06a-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de06a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de06a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de06a-150">CommonParameters</span></span>
<span data-ttu-id="de06a-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de06a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de06a-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de06a-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de06a-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de06a-153">INPUTS</span></span>

### <span data-ttu-id="de06a-154">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="de06a-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="de06a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="de06a-155">System.String</span></span>

## <span data-ttu-id="de06a-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de06a-156">OUTPUTS</span></span>

### <span data-ttu-id="de06a-157">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="de06a-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="de06a-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de06a-158">NOTES</span></span>

## <span data-ttu-id="de06a-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de06a-159">RELATED LINKS</span></span>
