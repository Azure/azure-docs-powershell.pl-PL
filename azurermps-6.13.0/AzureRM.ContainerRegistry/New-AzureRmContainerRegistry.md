---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: b70e4b4c184cfb6ebc5473cb0f49dec712bc62fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716446"
---
# <span data-ttu-id="ff3da-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff3da-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="ff3da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff3da-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3da-103">Tworzy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="ff3da-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff3da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff3da-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff3da-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ff3da-105">DESCRIPTION</span></span>
<span data-ttu-id="ff3da-106">Polecenie cmdlet New-AzureRmContainerRegistry powoduje utworzenie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ff3da-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="ff3da-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff3da-107">EXAMPLES</span></span>

### <span data-ttu-id="ff3da-108">Przykład 1: tworzenie rejestru kontenera za pomocą nowego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff3da-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ff3da-109">To polecenie tworzy rejestr kontenera przy użyciu nowego konta magazynu w grupie moja grupa zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="ff3da-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="ff3da-110">Przykład 2: tworzenie rejestru kontenera z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="ff3da-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ff3da-111">To polecenie tworzy rejestr kontenerowy z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="ff3da-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="ff3da-112">Przykład 3: tworzenie rejestru kontenera za pomocą istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff3da-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="ff3da-113">To polecenie tworzy rejestr kontenera z istniejącym kontem magazynu \` mystorageaccount \` w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ff3da-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="ff3da-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff3da-114">PARAMETERS</span></span>

### <span data-ttu-id="ff3da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3da-115">-DefaultProfile</span></span>
<span data-ttu-id="ff3da-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ff3da-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3da-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ff3da-117">-EnableAdminUser</span></span>
<span data-ttu-id="ff3da-118">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ff3da-118">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="ff3da-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ff3da-119">-Location</span></span>
<span data-ttu-id="ff3da-120">Lokalizacja rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ff3da-120">Container Registry Location.</span></span>
<span data-ttu-id="ff3da-121">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff3da-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="ff3da-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ff3da-122">-Name</span></span>
<span data-ttu-id="ff3da-123">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ff3da-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="ff3da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff3da-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff3da-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff3da-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff3da-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="ff3da-126">-Sku</span></span>
<span data-ttu-id="ff3da-127">Wersja SKU rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ff3da-127">Container Registry SKU.</span></span>
<span data-ttu-id="ff3da-128">Dozwolone wartości: podstawowe.</span><span class="sxs-lookup"><span data-stu-id="ff3da-128">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="ff3da-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff3da-129">-StorageAccountName</span></span>
<span data-ttu-id="ff3da-130">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff3da-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="ff3da-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff3da-131">-Tag</span></span>
<span data-ttu-id="ff3da-132">Znaczniki rejestru kontenera. pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ff3da-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="ff3da-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ff3da-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ff3da-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff3da-134">-Confirm</span></span>
<span data-ttu-id="ff3da-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff3da-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3da-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3da-136">-WhatIf</span></span>
<span data-ttu-id="ff3da-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff3da-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff3da-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff3da-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3da-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3da-139">CommonParameters</span></span>
<span data-ttu-id="ff3da-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3da-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3da-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3da-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3da-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff3da-142">INPUTS</span></span>

### <span data-ttu-id="ff3da-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ff3da-143">System.String</span></span>

## <span data-ttu-id="ff3da-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff3da-144">OUTPUTS</span></span>

### <span data-ttu-id="ff3da-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff3da-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ff3da-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff3da-146">NOTES</span></span>

## <span data-ttu-id="ff3da-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff3da-147">RELATED LINKS</span></span>

[<span data-ttu-id="ff3da-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff3da-148">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="ff3da-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff3da-149">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="ff3da-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff3da-150">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

