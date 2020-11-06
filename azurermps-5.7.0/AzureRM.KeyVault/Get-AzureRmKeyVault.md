---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554147"
---
# <span data-ttu-id="34847-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="34847-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="34847-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34847-102">SYNOPSIS</span></span>
<span data-ttu-id="34847-103">Pobiera kluczowe magazyny.</span><span class="sxs-lookup"><span data-stu-id="34847-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34847-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34847-104">SYNTAX</span></span>

### <span data-ttu-id="34847-105">ListAllVaultsInSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34847-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34847-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="34847-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34847-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="34847-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34847-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="34847-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34847-109">Opis</span><span class="sxs-lookup"><span data-stu-id="34847-109">DESCRIPTION</span></span>
<span data-ttu-id="34847-110">Polecenie cmdlet **Get-AzureRmKeyVault** pobiera informacje o najważniejszych magazynach w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="34847-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="34847-111">Możesz wyświetlić wszystkie wystąpienia najważniejszych magazynów w subskrypcji lub filtrować wyniki według grupy zasobów lub konkretnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="34847-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="34847-112">Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, w przypadku pojedynczego magazynu kluczy należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="34847-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="34847-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34847-113">EXAMPLES</span></span>

### <span data-ttu-id="34847-114">Przykład 1: pobieranie wszystkich najważniejszych magazynów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="34847-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="34847-115">To polecenie pobiera wszystkie kluczowe magazyny w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34847-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="34847-116">Przykład 2: uzyskiwanie określonego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="34847-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="34847-117">To polecenie pobiera kluczowy magazyn o nazwie Contoso03Vault w bieżącej subskrypcji, a następnie zapisuje go w zmiennej $MyVault.</span><span class="sxs-lookup"><span data-stu-id="34847-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="34847-118">Możesz sprawdzić właściwości $MyVault, aby uzyskać szczegółowe informacje o magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="34847-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="34847-119">Przykład 3: uzyskiwanie najważniejszych magazynów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="34847-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="34847-120">To polecenie pobiera wszystkie główne magazyny z grupy zasobów o nazwie ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="34847-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="34847-121">Przykład 4: pobieranie wszystkich usuniętych magazynów kluczy w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="34847-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="34847-122">To polecenie pobiera wszystkie usunięte magazyny kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="34847-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="34847-123">Przykład 5: uzyskiwanie usuniętego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="34847-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="34847-124">To polecenie pobiera usunięte informacje o magazynie kluczy o nazwie Contoso03Vault w bieżącej subskrypcji i w regionie eastus2.</span><span class="sxs-lookup"><span data-stu-id="34847-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="34847-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34847-125">PARAMETERS</span></span>

### <span data-ttu-id="34847-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34847-126">-DefaultProfile</span></span>
<span data-ttu-id="34847-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="34847-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34847-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="34847-128">-InRemovedState</span></span>
<span data-ttu-id="34847-129">Określa, czy w wyniku mają być pokazywane uprzednio usunięte magazyny.</span><span class="sxs-lookup"><span data-stu-id="34847-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34847-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="34847-130">-Location</span></span>
<span data-ttu-id="34847-131">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="34847-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34847-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34847-132">-ResourceGroupName</span></span>
<span data-ttu-id="34847-133">Określa nazwę grupy zasobów skojarzonej z badanym magazynem kluczy lub kluczami kluczy, których dotyczy zapytanie.</span><span class="sxs-lookup"><span data-stu-id="34847-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34847-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="34847-134">-Tag</span></span>
<span data-ttu-id="34847-135">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="34847-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="34847-136">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="34847-136">For example:</span></span>

<span data-ttu-id="34847-137">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="34847-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34847-138">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="34847-138">-VaultName</span></span>
<span data-ttu-id="34847-139">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="34847-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34847-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34847-140">CommonParameters</span></span>
<span data-ttu-id="34847-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34847-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34847-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34847-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34847-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34847-143">INPUTS</span></span>

### <span data-ttu-id="34847-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="34847-144">None</span></span>
<span data-ttu-id="34847-145">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="34847-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34847-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34847-146">OUTPUTS</span></span>

### <span data-ttu-id="34847-147">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="34847-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="34847-148">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. platforming. modele. PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="34847-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="34847-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="34847-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="34847-150">System. Collections. Generic. list "1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="34847-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="34847-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34847-151">NOTES</span></span>

## <span data-ttu-id="34847-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34847-152">RELATED LINKS</span></span>

[<span data-ttu-id="34847-153">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="34847-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="34847-154">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="34847-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
