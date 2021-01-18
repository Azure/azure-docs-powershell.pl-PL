---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: bff7a79513cc8eb0047860f9edd00c6c37c5f1b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498201"
---
# <span data-ttu-id="7f5d4-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7f5d4-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="7f5d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f5d4-103">Umożliwia usunięcie udziału plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="7f5d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f5d4-104">SYNTAX</span></span>

### <span data-ttu-id="7f5d4-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7f5d4-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f5d4-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="7f5d4-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f5d4-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="7f5d4-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f5d4-108">Nazwaudziału</span><span class="sxs-lookup"><span data-stu-id="7f5d4-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f5d4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7f5d4-109">DESCRIPTION</span></span>
<span data-ttu-id="7f5d4-110">Polecenie cmdlet **New-AzRmStorageShare** umożliwia usunięcie udziału plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="7f5d4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f5d4-111">EXAMPLES</span></span>

### <span data-ttu-id="7f5d4-112">Przykład 1: usuwanie udziału plików magazynu z nazwą konta magazynu i nazwą udziału</span><span class="sxs-lookup"><span data-stu-id="7f5d4-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="7f5d4-113">To polecenie usuwa udział plików magazynu z nazwą konta magazynu i nazwą udziału.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="7f5d4-114">Przykład 2: usuwanie udziału plików magazynu za pomocą obiektu konta magazynu i nazwy udziału</span><span class="sxs-lookup"><span data-stu-id="7f5d4-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="7f5d4-115">To polecenie usuwa udział plików magazynu z obiektem konta magazynu i nazwą udziału.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="7f5d4-116">Przykład 3: Usuwanie wszystkich udziałów plików magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="7f5d4-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="7f5d4-117">To polecenie usuwa wszystkie udziały plików magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="7f5d4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f5d4-118">PARAMETERS</span></span>

### <span data-ttu-id="7f5d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f5d4-119">-DefaultProfile</span></span>
<span data-ttu-id="7f5d4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7f5d4-121">-Force</span></span>
<span data-ttu-id="7f5d4-122">Wymuś usunięcie udziału i całej zawartości</span><span class="sxs-lookup"><span data-stu-id="7f5d4-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="7f5d4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f5d4-123">-InputObject</span></span>
<span data-ttu-id="7f5d4-124">Obiekt udostępniania magazynu</span><span class="sxs-lookup"><span data-stu-id="7f5d4-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d4-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f5d4-125">-Name</span></span>
<span data-ttu-id="7f5d4-126">Nazwa udziału</span><span class="sxs-lookup"><span data-stu-id="7f5d4-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f5d4-127">-PassThru</span></span>
<span data-ttu-id="7f5d4-128">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7f5d4-129">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7f5d4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f5d4-130">-ResourceGroupName</span></span>
<span data-ttu-id="7f5d4-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f5d4-132">-ResourceId</span></span>
<span data-ttu-id="7f5d4-133">Wprowadź identyfikator zasobu udziału pliku.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-133">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d4-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7f5d4-134">-StorageAccount</span></span>
<span data-ttu-id="7f5d4-135">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="7f5d4-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d4-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7f5d4-136">-StorageAccountName</span></span>
<span data-ttu-id="7f5d4-137">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5d4-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f5d4-138">-Confirm</span></span>
<span data-ttu-id="7f5d4-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f5d4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f5d4-140">-WhatIf</span></span>
<span data-ttu-id="7f5d4-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f5d4-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f5d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f5d4-143">CommonParameters</span></span>
<span data-ttu-id="7f5d4-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f5d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f5d4-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f5d4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f5d4-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f5d4-146">INPUTS</span></span>

### <span data-ttu-id="7f5d4-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7f5d4-147">System.String</span></span>

### <span data-ttu-id="7f5d4-148">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7f5d4-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7f5d4-149">Microsoft. Azure. Commands. Management. Storage. models. PSShare</span><span class="sxs-lookup"><span data-stu-id="7f5d4-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="7f5d4-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f5d4-150">OUTPUTS</span></span>

### <span data-ttu-id="7f5d4-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f5d4-151">System.Boolean</span></span>

## <span data-ttu-id="7f5d4-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f5d4-152">NOTES</span></span>

## <span data-ttu-id="7f5d4-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f5d4-153">RELATED LINKS</span></span>
