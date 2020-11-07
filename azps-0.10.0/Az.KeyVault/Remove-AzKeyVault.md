---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893033"
---
# <span data-ttu-id="cc11b-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="cc11b-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="cc11b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc11b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc11b-103">Usuwa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc11b-103">Deletes a key vault.</span></span>

## <span data-ttu-id="cc11b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc11b-104">SYNTAX</span></span>

### <span data-ttu-id="cc11b-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="cc11b-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc11b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="cc11b-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc11b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cc11b-107">DESCRIPTION</span></span>
<span data-ttu-id="cc11b-108">Polecenie cmdlet **Remove-AzKeyVault** usuwa określony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc11b-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="cc11b-109">Usuwane są również wszystkie klucze i klucze tajne zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="cc11b-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="cc11b-110">Pamiętaj, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy zapewnić lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="cc11b-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="cc11b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc11b-111">EXAMPLES</span></span>

### <span data-ttu-id="cc11b-112">Przykład 1: Usuwanie magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="cc11b-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="cc11b-113">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cc11b-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="cc11b-114">Przykład 2: Usuwanie magazynu kluczy z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cc11b-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="cc11b-115">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z grupy nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cc11b-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="cc11b-116">Jeśli nazwa grupy zasobów nie zostanie określona, polecenie cmdlet wyszukuje w bieżącym abonamentie nazwany Magazyn kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="cc11b-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="cc11b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc11b-117">PARAMETERS</span></span>

### <span data-ttu-id="cc11b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc11b-118">-AsJob</span></span>
<span data-ttu-id="cc11b-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cc11b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc11b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc11b-120">-DefaultProfile</span></span>
<span data-ttu-id="cc11b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cc11b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc11b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cc11b-122">-Force</span></span>
<span data-ttu-id="cc11b-123">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc11b-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="cc11b-124">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="cc11b-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="cc11b-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="cc11b-125">-InRemovedState</span></span>
<span data-ttu-id="cc11b-126">Trwale Usuń magazyn już usunięty.</span><span class="sxs-lookup"><span data-stu-id="cc11b-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc11b-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cc11b-127">-Location</span></span>
<span data-ttu-id="cc11b-128">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="cc11b-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="cc11b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc11b-129">-ResourceGroupName</span></span>
<span data-ttu-id="cc11b-130">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc11b-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cc11b-131">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="cc11b-131">-VaultName</span></span>
<span data-ttu-id="cc11b-132">Określa nazwę magazynu kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="cc11b-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="cc11b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc11b-133">-Confirm</span></span>
<span data-ttu-id="cc11b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc11b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc11b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc11b-135">-WhatIf</span></span>
<span data-ttu-id="cc11b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc11b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc11b-137">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc11b-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc11b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc11b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc11b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc11b-139">CommonParameters</span></span>
<span data-ttu-id="cc11b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc11b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc11b-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc11b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc11b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc11b-142">INPUTS</span></span>

### <span data-ttu-id="cc11b-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cc11b-143">None</span></span>
<span data-ttu-id="cc11b-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="cc11b-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc11b-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc11b-145">OUTPUTS</span></span>

## <span data-ttu-id="cc11b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc11b-146">NOTES</span></span>

## <span data-ttu-id="cc11b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc11b-147">RELATED LINKS</span></span>

[<span data-ttu-id="cc11b-148">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="cc11b-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="cc11b-149">Nowe — AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="cc11b-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
