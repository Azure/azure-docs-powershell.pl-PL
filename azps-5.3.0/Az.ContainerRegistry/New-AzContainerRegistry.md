---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503893"
---
# <span data-ttu-id="d8b91-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8b91-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="d8b91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8b91-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b91-103">Tworzy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="d8b91-103">Creates a container registry.</span></span>

## <span data-ttu-id="d8b91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8b91-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8b91-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8b91-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b91-106">Polecenie cmdlet New-AzContainerRegistry powoduje utworzenie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d8b91-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="d8b91-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8b91-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b91-108">Przykład 1: tworzenie rejestru kontenera za pomocą nowego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8b91-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d8b91-109">To polecenie tworzy rejestr kontenera przy użyciu nowego konta magazynu w grupie moja grupa zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="d8b91-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="d8b91-110">Przykład 2: tworzenie rejestru kontenera z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="d8b91-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="d8b91-111">To polecenie tworzy rejestr kontenerowy z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="d8b91-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="d8b91-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8b91-112">PARAMETERS</span></span>

### <span data-ttu-id="d8b91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b91-113">-DefaultProfile</span></span>
<span data-ttu-id="d8b91-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d8b91-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8b91-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="d8b91-115">-EnableAdminUser</span></span>
<span data-ttu-id="d8b91-116">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d8b91-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="d8b91-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d8b91-117">-Location</span></span>
<span data-ttu-id="d8b91-118">Lokalizacja rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d8b91-118">Container Registry Location.</span></span>
<span data-ttu-id="d8b91-119">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8b91-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="d8b91-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8b91-120">-Name</span></span>
<span data-ttu-id="d8b91-121">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d8b91-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="d8b91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b91-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8b91-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8b91-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="d8b91-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="d8b91-124">-Sku</span></span>
<span data-ttu-id="d8b91-125">Wersja SKU rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d8b91-125">Container Registry SKU.</span></span>
<span data-ttu-id="d8b91-126">Dozwolone wartości: podstawowe.</span><span class="sxs-lookup"><span data-stu-id="d8b91-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="d8b91-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8b91-127">-Tag</span></span>
<span data-ttu-id="d8b91-128">Znaczniki rejestru kontenera. pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="d8b91-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="d8b91-129">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="d8b91-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d8b91-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8b91-130">-Confirm</span></span>
<span data-ttu-id="d8b91-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8b91-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8b91-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b91-132">-WhatIf</span></span>
<span data-ttu-id="d8b91-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8b91-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b91-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8b91-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8b91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b91-135">CommonParameters</span></span>
<span data-ttu-id="d8b91-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b91-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8b91-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b91-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8b91-138">INPUTS</span></span>

### <span data-ttu-id="d8b91-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d8b91-139">System.String</span></span>

## <span data-ttu-id="d8b91-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8b91-140">OUTPUTS</span></span>

### <span data-ttu-id="d8b91-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8b91-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="d8b91-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8b91-142">NOTES</span></span>

## <span data-ttu-id="d8b91-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8b91-143">RELATED LINKS</span></span>

[<span data-ttu-id="d8b91-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8b91-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="d8b91-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8b91-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="d8b91-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d8b91-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

