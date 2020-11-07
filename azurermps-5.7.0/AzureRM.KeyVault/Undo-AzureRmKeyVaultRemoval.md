---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718919"
---
# <span data-ttu-id="f4394-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="f4394-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="f4394-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4394-102">SYNOPSIS</span></span>
<span data-ttu-id="f4394-103">Odkrycie usuniętego magazynu kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="f4394-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4394-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4394-104">SYNTAX</span></span>

### <span data-ttu-id="f4394-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f4394-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4394-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4394-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4394-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4394-107">DESCRIPTION</span></span>
<span data-ttu-id="f4394-108">Polecenie cmdlet **Undo-AzureRmKeyVaultRemoval** powoduje odzyskanie uprzednio usuniętego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="f4394-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="f4394-109">Odzyskany magazyn będzie aktywny po odzyskaniu</span><span class="sxs-lookup"><span data-stu-id="f4394-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="f4394-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4394-110">EXAMPLES</span></span>

### <span data-ttu-id="f4394-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f4394-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="f4394-112">To polecenie odzyska Magazyn kluczy "MyKeyVault", który został wcześniej usunięty z obszaru eastus2 i grupy zasobów "moja grupa zasobów", w stan aktywny i dostępny.</span><span class="sxs-lookup"><span data-stu-id="f4394-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="f4394-113">Znaczniki są również zastępowane nowym znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="f4394-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="f4394-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4394-114">PARAMETERS</span></span>

### <span data-ttu-id="f4394-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4394-115">-DefaultProfile</span></span>
<span data-ttu-id="f4394-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f4394-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4394-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4394-117">-InputObject</span></span>
<span data-ttu-id="f4394-118">Usunięto obiekt magazynu</span><span class="sxs-lookup"><span data-stu-id="f4394-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4394-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f4394-119">-Location</span></span>
<span data-ttu-id="f4394-120">Określa oryginalny region usługi Azure w magazynie usunięty.</span><span class="sxs-lookup"><span data-stu-id="f4394-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4394-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4394-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4394-122">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="f4394-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4394-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4394-123">-Tag</span></span>
<span data-ttu-id="f4394-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f4394-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f4394-125">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f4394-125">For example:</span></span>

<span data-ttu-id="f4394-126">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f4394-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4394-127">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="f4394-127">-VaultName</span></span>
<span data-ttu-id="f4394-128">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="f4394-128">Vault name.</span></span>
<span data-ttu-id="f4394-129">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="f4394-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4394-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4394-130">-Confirm</span></span>
<span data-ttu-id="f4394-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4394-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4394-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4394-132">-WhatIf</span></span>
<span data-ttu-id="f4394-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4394-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4394-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4394-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4394-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4394-135">CommonParameters</span></span>
<span data-ttu-id="f4394-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4394-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4394-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4394-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4394-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4394-138">INPUTS</span></span>

### <span data-ttu-id="f4394-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f4394-139">System.String</span></span>
<span data-ttu-id="f4394-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4394-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4394-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4394-141">OUTPUTS</span></span>

### <span data-ttu-id="f4394-142">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f4394-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f4394-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4394-143">NOTES</span></span>

## <span data-ttu-id="f4394-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4394-144">RELATED LINKS</span></span>

[<span data-ttu-id="f4394-145">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f4394-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="f4394-146">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f4394-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="f4394-147">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f4394-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
