---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 4d9b788637e0c97d8f129df33ac7e4050ce916d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963185"
---
# <span data-ttu-id="21618-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21618-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="21618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21618-102">SYNOPSIS</span></span>
<span data-ttu-id="21618-103">Tworzy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="21618-103">Creates a container registry.</span></span>

## <span data-ttu-id="21618-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21618-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21618-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="21618-105">DESCRIPTION</span></span>
<span data-ttu-id="21618-106">Polecenie New-AzContainerRegistry cmdlet tworzy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="21618-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="21618-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21618-107">EXAMPLES</span></span>

### <span data-ttu-id="21618-108">Przykład 1. Tworzenie rejestru kontenera przy użyciu nowego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="21618-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="21618-109">To polecenie tworzy rejestr kontenera z nowym kontem magazynu w grupie zasobów \` MyResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="21618-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="21618-110">Przykład 2. Tworzenie rejestru kontenera z włączonym użytkownikiem administratora.</span><span class="sxs-lookup"><span data-stu-id="21618-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="21618-111">To polecenie tworzy rejestr kontenera z włączonym użytkownikiem administratora.</span><span class="sxs-lookup"><span data-stu-id="21618-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="21618-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21618-112">PARAMETERS</span></span>

### <span data-ttu-id="21618-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21618-113">-DefaultProfile</span></span>
<span data-ttu-id="21618-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="21618-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21618-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="21618-115">-EnableAdminUser</span></span>
<span data-ttu-id="21618-116">Włącz dla użytkownika administratora rejestr kontenerów.</span><span class="sxs-lookup"><span data-stu-id="21618-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21618-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="21618-117">-Location</span></span>
<span data-ttu-id="21618-118">Container Registry Location (Lokalizacja rejestru kontenerów).</span><span class="sxs-lookup"><span data-stu-id="21618-118">Container Registry Location.</span></span>
<span data-ttu-id="21618-119">Domyślna lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21618-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="21618-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="21618-120">-Name</span></span>
<span data-ttu-id="21618-121">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="21618-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21618-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21618-122">-ResourceGroupName</span></span>
<span data-ttu-id="21618-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21618-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21618-124">- SKU</span><span class="sxs-lookup"><span data-stu-id="21618-124">-Sku</span></span>
<span data-ttu-id="21618-125">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="21618-125">Container Registry SKU.</span></span>
<span data-ttu-id="21618-126">Dozwolone wartości: Podstawowe.</span><span class="sxs-lookup"><span data-stu-id="21618-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21618-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="21618-127">-Tag</span></span>
<span data-ttu-id="21618-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="21618-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="21618-129">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="21618-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21618-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21618-130">-Confirm</span></span>
<span data-ttu-id="21618-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="21618-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21618-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21618-132">-WhatIf</span></span>
<span data-ttu-id="21618-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21618-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21618-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="21618-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21618-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21618-135">CommonParameters</span></span>
<span data-ttu-id="21618-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21618-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21618-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21618-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21618-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21618-138">INPUTS</span></span>

### <span data-ttu-id="21618-139">System.String</span><span class="sxs-lookup"><span data-stu-id="21618-139">System.String</span></span>

## <span data-ttu-id="21618-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21618-140">OUTPUTS</span></span>

### <span data-ttu-id="21618-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21618-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="21618-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21618-142">NOTES</span></span>

## <span data-ttu-id="21618-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21618-143">RELATED LINKS</span></span>

[<span data-ttu-id="21618-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21618-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="21618-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21618-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="21618-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="21618-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

