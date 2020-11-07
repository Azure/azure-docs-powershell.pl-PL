---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717325"
---
# <span data-ttu-id="e1170-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e1170-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="e1170-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1170-102">SYNOPSIS</span></span>
<span data-ttu-id="e1170-103">Usuwa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e1170-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1170-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1170-104">SYNTAX</span></span>

### <span data-ttu-id="e1170-105">ByAvailableVault (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1170-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1170-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="e1170-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1170-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="e1170-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1170-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="e1170-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1170-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e1170-109">DESCRIPTION</span></span>
<span data-ttu-id="e1170-110">Polecenie cmdlet **Remove-AzureRmKeyVault** usuwa określony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e1170-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="e1170-111">Usuwane są również wszystkie klucze i klucze tajne zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="e1170-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="e1170-112">Pamiętaj, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy zapewnić lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="e1170-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="e1170-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1170-113">EXAMPLES</span></span>

### <span data-ttu-id="e1170-114">Przykład 1: Usuwanie magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="e1170-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="e1170-115">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e1170-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="e1170-116">Przykład 2: Usuwanie magazynu kluczy z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e1170-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="e1170-117">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z grupy nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1170-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="e1170-118">Jeśli nazwa grupy zasobów nie zostanie określona, polecenie cmdlet wyszukuje w bieżącym abonamentie nazwany Magazyn kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e1170-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="e1170-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1170-119">PARAMETERS</span></span>

### <span data-ttu-id="e1170-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1170-120">-AsJob</span></span>
<span data-ttu-id="e1170-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e1170-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1170-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1170-122">-DefaultProfile</span></span>
<span data-ttu-id="e1170-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e1170-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1170-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e1170-124">-Force</span></span>
<span data-ttu-id="e1170-125">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e1170-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="e1170-126">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e1170-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1170-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e1170-127">-InputObject</span></span>
<span data-ttu-id="e1170-128">Obiekt magazynu kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e1170-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1170-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e1170-129">-InRemovedState</span></span>
<span data-ttu-id="e1170-130">Trwale Usuń magazyn już usunięty.</span><span class="sxs-lookup"><span data-stu-id="e1170-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1170-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e1170-131">-Location</span></span>
<span data-ttu-id="e1170-132">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="e1170-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="e1170-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1170-133">-PassThru</span></span>
<span data-ttu-id="e1170-134">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="e1170-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e1170-135">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e1170-135">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1170-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1170-136">-ResourceGroupName</span></span>
<span data-ttu-id="e1170-137">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1170-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1170-138">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="e1170-138">-VaultName</span></span>
<span data-ttu-id="e1170-139">Określa nazwę magazynu kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e1170-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1170-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1170-140">-Confirm</span></span>
<span data-ttu-id="e1170-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1170-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1170-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1170-142">-WhatIf</span></span>
<span data-ttu-id="e1170-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1170-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1170-144">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1170-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1170-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1170-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1170-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1170-146">CommonParameters</span></span>
<span data-ttu-id="e1170-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1170-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1170-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1170-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1170-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1170-149">INPUTS</span></span>

### <span data-ttu-id="e1170-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1170-150">None</span></span>
<span data-ttu-id="e1170-151">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e1170-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1170-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1170-152">OUTPUTS</span></span>

### <span data-ttu-id="e1170-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1170-153">System.Boolean</span></span>

## <span data-ttu-id="e1170-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1170-154">NOTES</span></span>

## <span data-ttu-id="e1170-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1170-155">RELATED LINKS</span></span>

[<span data-ttu-id="e1170-156">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e1170-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="e1170-157">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e1170-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
