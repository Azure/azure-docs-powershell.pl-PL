---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718191"
---
# <span data-ttu-id="47e59-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="47e59-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="47e59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47e59-102">SYNOPSIS</span></span>
<span data-ttu-id="47e59-103">Odkrycie usuniętego magazynu kluczy w stanie aktywnym.</span><span class="sxs-lookup"><span data-stu-id="47e59-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47e59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47e59-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e59-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47e59-105">DESCRIPTION</span></span>
<span data-ttu-id="47e59-106">Polecenie cmdlet **Undo-AzureRmKeyVaultRemoval** powoduje odzyskanie uprzednio usuniętego magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="47e59-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="47e59-107">Odzyskany magazyn będzie aktywny po odzyskaniu</span><span class="sxs-lookup"><span data-stu-id="47e59-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="47e59-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47e59-108">EXAMPLES</span></span>

### <span data-ttu-id="47e59-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47e59-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="47e59-110">To polecenie odzyska Magazyn kluczy "MyKeyVault", który został wcześniej usunięty z obszaru eastus2 i grupy zasobów "moja grupa zasobów", w stan aktywny i dostępny.</span><span class="sxs-lookup"><span data-stu-id="47e59-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="47e59-111">Znaczniki są również zastępowane nowym znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="47e59-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="47e59-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47e59-112">PARAMETERS</span></span>

### <span data-ttu-id="47e59-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="47e59-113">-Location</span></span>
<span data-ttu-id="47e59-114">Określa oryginalny region usługi Azure w magazynie usunięty.</span><span class="sxs-lookup"><span data-stu-id="47e59-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e59-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e59-115">-ResourceGroupName</span></span>
<span data-ttu-id="47e59-116">Określa nazwę istniejącej grupy zasobów, w której ma zostać utworzony magazyn kluczy.</span><span class="sxs-lookup"><span data-stu-id="47e59-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="47e59-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="47e59-117">-Tag</span></span>
<span data-ttu-id="47e59-118">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="47e59-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="47e59-119">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="47e59-119">For example:</span></span>

<span data-ttu-id="47e59-120">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="47e59-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e59-121">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="47e59-121">-VaultName</span></span>
<span data-ttu-id="47e59-122">Nazwa magazynu.</span><span class="sxs-lookup"><span data-stu-id="47e59-122">Vault name.</span></span>
<span data-ttu-id="47e59-123">Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="47e59-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="47e59-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47e59-124">-Confirm</span></span>
<span data-ttu-id="47e59-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e59-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e59-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e59-126">-WhatIf</span></span>
<span data-ttu-id="47e59-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e59-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47e59-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47e59-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e59-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e59-129">-DefaultProfile</span></span>
<span data-ttu-id="47e59-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47e59-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47e59-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e59-131">CommonParameters</span></span>
<span data-ttu-id="47e59-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e59-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e59-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e59-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e59-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47e59-134">INPUTS</span></span>

### <span data-ttu-id="47e59-135">System. String</span><span class="sxs-lookup"><span data-stu-id="47e59-135">System.String</span></span>
<span data-ttu-id="47e59-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="47e59-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="47e59-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47e59-137">OUTPUTS</span></span>

### <span data-ttu-id="47e59-138">Microsoft. Azure. Commands. platforming. models. PSVault</span><span class="sxs-lookup"><span data-stu-id="47e59-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="47e59-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47e59-139">NOTES</span></span>

## <span data-ttu-id="47e59-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47e59-140">RELATED LINKS</span></span>

[<span data-ttu-id="47e59-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="47e59-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="47e59-142">Nowe — AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="47e59-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="47e59-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="47e59-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
