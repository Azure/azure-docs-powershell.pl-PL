---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: ca2db2ece85860c9aeae8e45909cdb5135beaae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997270"
---
# <span data-ttu-id="aa347-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="aa347-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="aa347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa347-102">SYNOPSIS</span></span>
<span data-ttu-id="aa347-103">Usuwa udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa347-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="aa347-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa347-104">SYNTAX</span></span>

### <span data-ttu-id="aa347-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="aa347-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa347-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="aa347-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa347-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="aa347-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa347-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="aa347-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa347-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa347-109">DESCRIPTION</span></span>
<span data-ttu-id="aa347-110">Polecenie **cmdlet New-AzRmStorageShare** usuwa udział plików magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa347-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="aa347-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa347-111">EXAMPLES</span></span>

### <span data-ttu-id="aa347-112">Przykład 1. Usuwanie udziału plików magazynu z nazwą konta magazynu i nazwą udostępniania</span><span class="sxs-lookup"><span data-stu-id="aa347-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="aa347-113">To polecenie usuwa udział plików magazynu z nazwą konta magazynu i nazwą udostępniania.</span><span class="sxs-lookup"><span data-stu-id="aa347-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="aa347-114">Przykład 2. Usuwanie udziału plików magazynu z obiektem konta magazynu i nazwą udostępniania</span><span class="sxs-lookup"><span data-stu-id="aa347-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="aa347-115">To polecenie usuwa udział plików magazynu z obiektem konta magazynu i nazwę udostępniania.</span><span class="sxs-lookup"><span data-stu-id="aa347-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="aa347-116">Przykład 3. Usuwanie wszystkich udziałów plików magazynu w koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="aa347-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="aa347-117">To polecenie usuwa wszystkie udziały plików magazynu w koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="aa347-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="aa347-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa347-118">PARAMETERS</span></span>

### <span data-ttu-id="aa347-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa347-119">-DefaultProfile</span></span>
<span data-ttu-id="aa347-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa347-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa347-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="aa347-121">-Force</span></span>
<span data-ttu-id="aa347-122">Wymuszanie usunięcia udostępniania i całej jego zawartości</span><span class="sxs-lookup"><span data-stu-id="aa347-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="aa347-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa347-123">-InputObject</span></span>
<span data-ttu-id="aa347-124">Obiekt Współużytk magazynowania</span><span class="sxs-lookup"><span data-stu-id="aa347-124">Storage Share object</span></span>

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

### <span data-ttu-id="aa347-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aa347-125">-Name</span></span>
<span data-ttu-id="aa347-126">Nazwa udostępniania</span><span class="sxs-lookup"><span data-stu-id="aa347-126">Share Name</span></span>

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

### <span data-ttu-id="aa347-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa347-127">-PassThru</span></span>
<span data-ttu-id="aa347-128">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="aa347-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="aa347-129">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="aa347-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="aa347-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa347-130">-ResourceGroupName</span></span>
<span data-ttu-id="aa347-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa347-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="aa347-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa347-132">-ResourceId</span></span>
<span data-ttu-id="aa347-133">Wprowadź identyfikator zasobu udziału plików.</span><span class="sxs-lookup"><span data-stu-id="aa347-133">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="aa347-134">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa347-134">-StorageAccount</span></span>
<span data-ttu-id="aa347-135">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="aa347-135">Storage account object</span></span>

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

### <span data-ttu-id="aa347-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa347-136">-StorageAccountName</span></span>
<span data-ttu-id="aa347-137">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="aa347-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="aa347-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa347-138">-Confirm</span></span>
<span data-ttu-id="aa347-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa347-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa347-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa347-140">-WhatIf</span></span>
<span data-ttu-id="aa347-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa347-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa347-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aa347-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa347-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa347-143">CommonParameters</span></span>
<span data-ttu-id="aa347-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa347-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa347-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa347-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa347-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa347-146">INPUTS</span></span>

### <span data-ttu-id="aa347-147">System.String</span><span class="sxs-lookup"><span data-stu-id="aa347-147">System.String</span></span>

### <span data-ttu-id="aa347-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa347-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="aa347-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="aa347-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="aa347-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa347-150">OUTPUTS</span></span>

### <span data-ttu-id="aa347-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa347-151">System.Boolean</span></span>

## <span data-ttu-id="aa347-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa347-152">NOTES</span></span>

## <span data-ttu-id="aa347-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa347-153">RELATED LINKS</span></span>
