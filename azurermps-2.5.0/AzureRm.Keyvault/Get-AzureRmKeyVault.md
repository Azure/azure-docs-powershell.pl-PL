---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 7cbcf722b71919096ca2c7d1dc3201ad2fe42f2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898919"
---
# <span data-ttu-id="ed5e7-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed5e7-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="ed5e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5e7-103">Pobiera kluczowe magazyny.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed5e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed5e7-104">SYNTAX</span></span>

### <span data-ttu-id="ed5e7-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="ed5e7-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed5e7-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="ed5e7-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed5e7-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed5e7-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed5e7-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="ed5e7-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed5e7-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="ed5e7-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed5e7-110">Opis</span><span class="sxs-lookup"><span data-stu-id="ed5e7-110">DESCRIPTION</span></span>
<span data-ttu-id="ed5e7-111">Polecenie cmdlet **Get-AzureRmKeyVault** pobiera informacje o najważniejszych magazynach w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="ed5e7-112">Możesz wyświetlić wszystkie wystąpienia najważniejszych magazynów w subskrypcji lub filtrować wyniki według grupy zasobów lub konkretnego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="ed5e7-113">Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, w przypadku pojedynczego magazynu kluczy należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="ed5e7-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed5e7-114">EXAMPLES</span></span>

### <span data-ttu-id="ed5e7-115">Przykład 1: pobieranie wszystkich najważniejszych magazynów w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ed5e7-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="ed5e7-116">To polecenie pobiera wszystkie kluczowe magazyny w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="ed5e7-117">Przykład 2: uzyskiwanie określonego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="ed5e7-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="ed5e7-118">To polecenie pobiera kluczowy magazyn o nazwie Contoso03Vault w bieżącej subskrypcji, a następnie zapisuje go w zmiennej $MyVault.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="ed5e7-119">Możesz sprawdzić właściwości $MyVault, aby uzyskać szczegółowe informacje o magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="ed5e7-120">Przykład 3: uzyskiwanie najważniejszych magazynów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ed5e7-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="ed5e7-121">To polecenie pobiera wszystkie główne magazyny z grupy zasobów o nazwie ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="ed5e7-122">Przykład 4: pobieranie wszystkich usuniętych magazynów kluczy w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ed5e7-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="ed5e7-123">To polecenie pobiera wszystkie usunięte magazyny kluczy w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="ed5e7-124">Przykład 5: uzyskiwanie usuniętego magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="ed5e7-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="ed5e7-125">To polecenie pobiera usunięte informacje o magazynie kluczy o nazwie Contoso03Vault w bieżącej subskrypcji i w regionie eastus2.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="ed5e7-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed5e7-126">PARAMETERS</span></span>

### <span data-ttu-id="ed5e7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5e7-127">-DefaultProfile</span></span>
<span data-ttu-id="ed5e7-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ed5e7-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed5e7-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ed5e7-129">-InRemovedState</span></span>
<span data-ttu-id="ed5e7-130">Określa, czy w wyniku mają być pokazywane uprzednio usunięte magazyny.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="ed5e7-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ed5e7-131">-Location</span></span>
<span data-ttu-id="ed5e7-132">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5e7-133">-ResourceGroupName</span></span>
<span data-ttu-id="ed5e7-134">Określa nazwę grupy zasobów skojarzonej z badanym magazynem kluczy lub kluczami kluczy, których dotyczy zapytanie.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e7-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed5e7-135">-Tag</span></span>
<span data-ttu-id="ed5e7-136">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ed5e7-137">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="ed5e7-137">For example:</span></span>

<span data-ttu-id="ed5e7-138">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ed5e7-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ed5e7-139">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="ed5e7-139">-VaultName</span></span>
<span data-ttu-id="ed5e7-140">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5e7-141">CommonParameters</span></span>
<span data-ttu-id="ed5e7-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5e7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5e7-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed5e7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5e7-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed5e7-144">INPUTS</span></span>

## <span data-ttu-id="ed5e7-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed5e7-145">OUTPUTS</span></span>

### <span data-ttu-id="ed5e7-146">Microsoft. Azure. Commands. platforming. models. PSVault</span><span class="sxs-lookup"><span data-stu-id="ed5e7-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="ed5e7-147">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. platforming. modele. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="ed5e7-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="ed5e7-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="ed5e7-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="ed5e7-149">System. Collections. Generic. list "1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="ed5e7-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="ed5e7-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed5e7-150">NOTES</span></span>

## <span data-ttu-id="ed5e7-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed5e7-151">RELATED LINKS</span></span>

[<span data-ttu-id="ed5e7-152">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed5e7-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="ed5e7-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed5e7-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
