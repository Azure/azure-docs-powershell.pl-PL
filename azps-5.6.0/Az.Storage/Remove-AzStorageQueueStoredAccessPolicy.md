---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 88b142943e37009cf21b35bdaadfd209d1d74c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961274"
---
# <span data-ttu-id="38cb3-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38cb3-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="38cb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="38cb3-103">Usuwa przechowywane zasady dostępu z kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb3-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="38cb3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="38cb3-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38cb3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="38cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="38cb3-106">Polecenie **cmdlet Remove-AzStorageQueueStoredAccessPolicy** usuwa przechowywane zasady dostępu z kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb3-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="38cb3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="38cb3-107">EXAMPLES</span></span>

### <span data-ttu-id="38cb3-108">Przykład 1. Usuwanie przechowywanych zasad dostępu z kolejki magazynu</span><span class="sxs-lookup"><span data-stu-id="38cb3-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="38cb3-109">To polecenie usuwa zasady dostępu o nazwie Zasady04 z kolejki magazynu o nazwie Moje kolejkowanie.</span><span class="sxs-lookup"><span data-stu-id="38cb3-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="38cb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38cb3-110">PARAMETERS</span></span>

### <span data-ttu-id="38cb3-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="38cb3-111">-Context</span></span>
<span data-ttu-id="38cb3-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="38cb3-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cb3-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38cb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38cb3-114">-DefaultProfile</span></span>
<span data-ttu-id="38cb3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38cb3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38cb3-116">-PassThru</span></span>
<span data-ttu-id="38cb3-117">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="38cb3-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="38cb3-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="38cb3-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="38cb3-119">— Zasady</span><span class="sxs-lookup"><span data-stu-id="38cb3-119">-Policy</span></span>
<span data-ttu-id="38cb3-120">Określa nazwę przechowywanych zasad dostępu usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cb3-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38cb3-121">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="38cb3-121">-Queue</span></span>
<span data-ttu-id="38cb3-122">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb3-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38cb3-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38cb3-123">-Confirm</span></span>
<span data-ttu-id="38cb3-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="38cb3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38cb3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38cb3-125">-WhatIf</span></span>
<span data-ttu-id="38cb3-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cb3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38cb3-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="38cb3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38cb3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38cb3-128">CommonParameters</span></span>
<span data-ttu-id="38cb3-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38cb3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38cb3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38cb3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38cb3-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38cb3-131">INPUTS</span></span>

### <span data-ttu-id="38cb3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="38cb3-132">System.String</span></span>

### <span data-ttu-id="38cb3-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="38cb3-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38cb3-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38cb3-134">OUTPUTS</span></span>

### <span data-ttu-id="38cb3-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38cb3-135">System.Boolean</span></span>

## <span data-ttu-id="38cb3-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="38cb3-136">NOTES</span></span>

## <span data-ttu-id="38cb3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38cb3-137">RELATED LINKS</span></span>

[<span data-ttu-id="38cb3-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38cb3-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="38cb3-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="38cb3-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="38cb3-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38cb3-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="38cb3-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38cb3-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
