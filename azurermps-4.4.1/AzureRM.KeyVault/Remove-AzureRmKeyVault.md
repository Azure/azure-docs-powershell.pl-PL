---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551851"
---
# <span data-ttu-id="e95d9-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e95d9-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="e95d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e95d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e95d9-103">Usuwa Magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e95d9-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e95d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e95d9-104">SYNTAX</span></span>

### <span data-ttu-id="e95d9-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="e95d9-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95d9-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="e95d9-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e95d9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e95d9-107">DESCRIPTION</span></span>
<span data-ttu-id="e95d9-108">Polecenie cmdlet **Remove-AzureRmKeyVault** usuwa określony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="e95d9-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="e95d9-109">Usuwane są również wszystkie klucze i klucze tajne zawarte w tym wystąpieniu.</span><span class="sxs-lookup"><span data-stu-id="e95d9-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="e95d9-110">Pamiętaj, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, należy zapewnić lepszą wydajność.</span><span class="sxs-lookup"><span data-stu-id="e95d9-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="e95d9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e95d9-111">EXAMPLES</span></span>

### <span data-ttu-id="e95d9-112">Przykład 1: Usuwanie magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="e95d9-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="e95d9-113">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e95d9-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="e95d9-114">Przykład 2: Usuwanie magazynu kluczy z określonej grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e95d9-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="e95d9-115">To polecenie usuwa Magazyn kluczy o nazwie Contoso03Vault z grupy nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e95d9-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="e95d9-116">Jeśli nazwa grupy zasobów nie zostanie określona, polecenie cmdlet wyszukuje w bieżącym abonamentie nazwany Magazyn kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e95d9-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="e95d9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e95d9-117">PARAMETERS</span></span>

### <span data-ttu-id="e95d9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e95d9-118">-Force</span></span>
<span data-ttu-id="e95d9-119">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e95d9-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="e95d9-120">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru usunięcia magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e95d9-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95d9-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e95d9-121">-InRemovedState</span></span>
<span data-ttu-id="e95d9-122">Trwale Usuń magazyn już usunięty.</span><span class="sxs-lookup"><span data-stu-id="e95d9-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e95d9-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e95d9-123">-Location</span></span>
<span data-ttu-id="e95d9-124">Lokalizacja usuniętego magazynu.</span><span class="sxs-lookup"><span data-stu-id="e95d9-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e95d9-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e95d9-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d9-127">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="e95d9-127">-VaultName</span></span>
<span data-ttu-id="e95d9-128">Określa nazwę magazynu kluczy, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e95d9-128">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95d9-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e95d9-129">-Confirm</span></span>
<span data-ttu-id="e95d9-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95d9-131">-WhatIf</span></span>
<span data-ttu-id="e95d9-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95d9-133">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e95d9-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95d9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e95d9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95d9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95d9-135">-DefaultProfile</span></span>
<span data-ttu-id="e95d9-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e95d9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e95d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95d9-137">CommonParameters</span></span>
<span data-ttu-id="e95d9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95d9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95d9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95d9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e95d9-140">INPUTS</span></span>

## <span data-ttu-id="e95d9-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e95d9-141">OUTPUTS</span></span>

## <span data-ttu-id="e95d9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e95d9-142">NOTES</span></span>

## <span data-ttu-id="e95d9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e95d9-143">RELATED LINKS</span></span>

[<span data-ttu-id="e95d9-144">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e95d9-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="e95d9-145">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="e95d9-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
