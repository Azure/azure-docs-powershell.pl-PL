---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 1c546894cf9b11dcb65fb12b9b0575e2fd3191fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894838"
---
# <span data-ttu-id="668b2-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="668b2-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="668b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="668b2-102">SYNOPSIS</span></span>
<span data-ttu-id="668b2-103">Tworzy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="668b2-103">Creates a container registry.</span></span>

## <span data-ttu-id="668b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="668b2-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="668b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="668b2-105">DESCRIPTION</span></span>
<span data-ttu-id="668b2-106">Polecenie cmdlet New-AzContainerRegistry powoduje utworzenie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="668b2-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="668b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="668b2-107">EXAMPLES</span></span>

### <span data-ttu-id="668b2-108">Przykład 1: tworzenie rejestru kontenera za pomocą nowego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="668b2-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="668b2-109">To polecenie tworzy rejestr kontenera przy użyciu nowego konta magazynu w grupie moja grupa zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="668b2-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="668b2-110">Przykład 2: tworzenie rejestru kontenera z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="668b2-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="668b2-111">To polecenie tworzy rejestr kontenerowy z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="668b2-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="668b2-112">Przykład 3: tworzenie rejestru kontenera za pomocą istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="668b2-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="668b2-113">To polecenie tworzy rejestr kontenera z istniejącym kontem magazynu \` mystorageaccount \` w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="668b2-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="668b2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="668b2-114">PARAMETERS</span></span>

### <span data-ttu-id="668b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668b2-115">-DefaultProfile</span></span>
<span data-ttu-id="668b2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="668b2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="668b2-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="668b2-117">-EnableAdminUser</span></span>
<span data-ttu-id="668b2-118">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="668b2-118">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="668b2-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="668b2-119">-Location</span></span>
<span data-ttu-id="668b2-120">Lokalizacja rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="668b2-120">Container Registry Location.</span></span>
<span data-ttu-id="668b2-121">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="668b2-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="668b2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="668b2-122">-Name</span></span>
<span data-ttu-id="668b2-123">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="668b2-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="668b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="668b2-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="668b2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="668b2-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="668b2-126">-Sku</span></span>
<span data-ttu-id="668b2-127">Wersja SKU rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="668b2-127">Container Registry SKU.</span></span>
<span data-ttu-id="668b2-128">Dozwolone wartości: podstawowe.</span><span class="sxs-lookup"><span data-stu-id="668b2-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668b2-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="668b2-129">-StorageAccountName</span></span>
<span data-ttu-id="668b2-130">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="668b2-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="668b2-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="668b2-131">-Tag</span></span>
<span data-ttu-id="668b2-132">Znaczniki rejestru kontenera. pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="668b2-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="668b2-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="668b2-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="668b2-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="668b2-134">-Confirm</span></span>
<span data-ttu-id="668b2-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="668b2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668b2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="668b2-136">-WhatIf</span></span>
<span data-ttu-id="668b2-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="668b2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668b2-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="668b2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="668b2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668b2-139">CommonParameters</span></span>
<span data-ttu-id="668b2-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="668b2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668b2-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="668b2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668b2-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="668b2-142">INPUTS</span></span>

### <span data-ttu-id="668b2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="668b2-143">System.String</span></span>

## <span data-ttu-id="668b2-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="668b2-144">OUTPUTS</span></span>

### <span data-ttu-id="668b2-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="668b2-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="668b2-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="668b2-146">NOTES</span></span>

## <span data-ttu-id="668b2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="668b2-147">RELATED LINKS</span></span>

[<span data-ttu-id="668b2-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="668b2-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="668b2-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="668b2-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="668b2-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="668b2-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

