---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 32bf76e80dbd088b133d4401dc51bb1f49b2593b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707529"
---
# <span data-ttu-id="e3b30-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b30-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e3b30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3b30-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b30-103">Usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e3b30-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="e3b30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3b30-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b30-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3b30-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b30-106">Polecenie cmdlet **Remove-AzStorageQueueStoredAccessPolicy** usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e3b30-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="e3b30-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3b30-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b30-108">Przykład 1: usuwanie zapisanych zasad dostępu z kolejki magazynu</span><span class="sxs-lookup"><span data-stu-id="e3b30-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="e3b30-109">To polecenie usuwa zasady dostępu o nazwie Policy04 z kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="e3b30-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="e3b30-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3b30-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b30-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e3b30-111">-Context</span></span>
<span data-ttu-id="e3b30-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e3b30-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e3b30-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e3b30-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e3b30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b30-114">-DefaultProfile</span></span>
<span data-ttu-id="e3b30-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b30-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3b30-116">-PassThru</span></span>
<span data-ttu-id="e3b30-117">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="e3b30-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e3b30-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="e3b30-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e3b30-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="e3b30-119">-Policy</span></span>
<span data-ttu-id="e3b30-120">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3b30-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e3b30-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="e3b30-121">-Queue</span></span>
<span data-ttu-id="e3b30-122">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b30-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="e3b30-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3b30-123">-Confirm</span></span>
<span data-ttu-id="e3b30-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3b30-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b30-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b30-125">-WhatIf</span></span>
<span data-ttu-id="e3b30-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3b30-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b30-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3b30-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b30-128">CommonParameters</span></span>
<span data-ttu-id="e3b30-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b30-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b30-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3b30-131">INPUTS</span></span>

### <span data-ttu-id="e3b30-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b30-132">System.String</span></span>

### <span data-ttu-id="e3b30-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e3b30-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e3b30-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3b30-134">OUTPUTS</span></span>

### <span data-ttu-id="e3b30-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3b30-135">System.Boolean</span></span>

## <span data-ttu-id="e3b30-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3b30-136">NOTES</span></span>

## <span data-ttu-id="e3b30-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3b30-137">RELATED LINKS</span></span>

[<span data-ttu-id="e3b30-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b30-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e3b30-139">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e3b30-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e3b30-140">Nowe — AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b30-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e3b30-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b30-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)