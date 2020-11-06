---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526902"
---
# <span data-ttu-id="7e13b-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e13b-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="7e13b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e13b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e13b-103">Tworzy rejestr kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e13b-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e13b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e13b-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e13b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7e13b-105">DESCRIPTION</span></span>
<span data-ttu-id="7e13b-106">Polecenie cmdlet New-AzureRmContainerRegistry powoduje utworzenie rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e13b-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="7e13b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e13b-107">EXAMPLES</span></span>

### <span data-ttu-id="7e13b-108">Przykład 1: tworzenie rejestru kontenera za pomocą nowego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7e13b-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="7e13b-109">To polecenie tworzy rejestr kontenera przy użyciu nowego konta magazynu w grupie moja grupa zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="7e13b-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="7e13b-110">Przykład 2: tworzenie rejestru kontenera z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="7e13b-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="7e13b-111">To polecenie tworzy rejestr kontenerowy z włączonym użytkownikiem administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="7e13b-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="7e13b-112">Przykład 3: tworzenie rejestru kontenera za pomocą istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7e13b-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="7e13b-113">To polecenie tworzy rejestr kontenera z istniejącym kontem magazynu \` mystorageaccount \` w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7e13b-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="7e13b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e13b-114">PARAMETERS</span></span>

### <span data-ttu-id="7e13b-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="7e13b-115">-EnableAdminUser</span></span>
<span data-ttu-id="7e13b-116">Włącz użytkownika administracyjnego dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e13b-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7e13b-117">-Location</span></span>
<span data-ttu-id="7e13b-118">Lokalizacja rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e13b-118">Container Registry Location.</span></span>
<span data-ttu-id="7e13b-119">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e13b-119">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e13b-120">-Name</span></span>
<span data-ttu-id="7e13b-121">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e13b-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e13b-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e13b-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e13b-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="7e13b-124">-Sku</span></span>
<span data-ttu-id="7e13b-125">Wersja SKU rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7e13b-125">Container Registry SKU.</span></span>
<span data-ttu-id="7e13b-126">Dozwolone wartości: podstawowe.</span><span class="sxs-lookup"><span data-stu-id="7e13b-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e13b-127">-StorageAccountName</span></span>
<span data-ttu-id="7e13b-128">Nazwa istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7e13b-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e13b-129">-Tag</span></span>
<span data-ttu-id="7e13b-130">Znaczniki rejestru kontenera. pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="7e13b-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="7e13b-131">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="7e13b-131">For example:</span></span>

<span data-ttu-id="7e13b-132">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="7e13b-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e13b-133">-Confirm</span></span>
<span data-ttu-id="7e13b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e13b-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e13b-135">-WhatIf</span></span>
<span data-ttu-id="7e13b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e13b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e13b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e13b-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e13b-138">-DefaultProfile</span></span>
<span data-ttu-id="7e13b-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7e13b-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e13b-140">CommonParameters</span></span>
<span data-ttu-id="7e13b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e13b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e13b-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e13b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e13b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e13b-143">INPUTS</span></span>

### <span data-ttu-id="7e13b-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7e13b-144">None</span></span>
<span data-ttu-id="7e13b-145">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7e13b-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e13b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e13b-146">OUTPUTS</span></span>

### <span data-ttu-id="7e13b-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e13b-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="7e13b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e13b-148">NOTES</span></span>

## <span data-ttu-id="7e13b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e13b-149">RELATED LINKS</span></span>

[<span data-ttu-id="7e13b-150">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e13b-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="7e13b-151">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e13b-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="7e13b-152">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e13b-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

