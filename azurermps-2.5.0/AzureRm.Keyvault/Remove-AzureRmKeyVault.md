---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897362"
---
# <span data-ttu-id="09778-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="09778-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="09778-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09778-102">SYNOPSIS</span></span>
<span data-ttu-id="09778-103">Usuwa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="09778-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09778-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09778-104">SYNTAX</span></span>

### <span data-ttu-id="09778-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="09778-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09778-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="09778-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09778-107">Opis</span><span class="sxs-lookup"><span data-stu-id="09778-107">DESCRIPTION</span></span>
<span data-ttu-id="09778-108">Polecenie cmdlet **Remove-AzureRmKeyVault** usuwa określony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="09778-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="09778-109">Usuwane są również wszystkie klucze i klucze tajne zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="09778-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="09778-110">Pamiętaj, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy zapewnić lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="09778-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="09778-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09778-111">EXAMPLES</span></span>

### <span data-ttu-id="09778-112">Przykład 1: Usuwanie magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="09778-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="09778-113">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="09778-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="09778-114">Przykład 2: Usuwanie magazynu kluczy z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="09778-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="09778-115">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z grupy nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="09778-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="09778-116">Jeśli nazwa grupy zasobów nie zostanie określona, polecenie cmdlet wyszukuje w bieżącym abonamentie nazwany Magazyn kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="09778-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="09778-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09778-117">PARAMETERS</span></span>

### <span data-ttu-id="09778-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09778-118">-AsJob</span></span>
<span data-ttu-id="09778-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="09778-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09778-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09778-120">-DefaultProfile</span></span>
<span data-ttu-id="09778-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="09778-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09778-122">-Force</span><span class="sxs-lookup"><span data-stu-id="09778-122">-Force</span></span>
<span data-ttu-id="09778-123">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="09778-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="09778-124">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="09778-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="09778-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="09778-125">-InRemovedState</span></span>
<span data-ttu-id="09778-126">Trwale Usuń magazyn już usunięty.</span><span class="sxs-lookup"><span data-stu-id="09778-126">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="09778-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="09778-127">-Location</span></span>
<span data-ttu-id="09778-128">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="09778-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="09778-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09778-129">-ResourceGroupName</span></span>
<span data-ttu-id="09778-130">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09778-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09778-131">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="09778-131">-VaultName</span></span>
<span data-ttu-id="09778-132">Określa nazwę magazynu kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="09778-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="09778-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09778-133">-Confirm</span></span>
<span data-ttu-id="09778-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09778-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09778-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09778-135">-WhatIf</span></span>
<span data-ttu-id="09778-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09778-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09778-137">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09778-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09778-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09778-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09778-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09778-139">CommonParameters</span></span>
<span data-ttu-id="09778-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09778-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09778-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09778-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09778-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09778-142">INPUTS</span></span>

## <span data-ttu-id="09778-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09778-143">OUTPUTS</span></span>

## <span data-ttu-id="09778-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09778-144">NOTES</span></span>

## <span data-ttu-id="09778-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09778-145">RELATED LINKS</span></span>

[<span data-ttu-id="09778-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="09778-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="09778-147">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="09778-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
