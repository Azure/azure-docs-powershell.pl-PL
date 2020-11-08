---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224769"
---
# <span data-ttu-id="4843a-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4843a-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="4843a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4843a-102">SYNOPSIS</span></span>
<span data-ttu-id="4843a-103">Usuwa kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="4843a-103">Removes a storage queue.</span></span>

## <span data-ttu-id="4843a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4843a-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4843a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4843a-105">DESCRIPTION</span></span>
<span data-ttu-id="4843a-106">Polecenie cmdlet **Remove-AzStorageQueue** umożliwia usunięcie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="4843a-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="4843a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4843a-107">EXAMPLES</span></span>

### <span data-ttu-id="4843a-108">Przykład 1: usuwanie kolejki magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="4843a-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="4843a-109">To polecenie umożliwia usunięcie kolejki o nazwie ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="4843a-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="4843a-110">Przykład 2: usuwanie wielu kolejek magazynowania</span><span class="sxs-lookup"><span data-stu-id="4843a-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="4843a-111">To polecenie usuwa wszystkie kolejki o nazwach rozpoczynających się od contoso.</span><span class="sxs-lookup"><span data-stu-id="4843a-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="4843a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4843a-112">PARAMETERS</span></span>

### <span data-ttu-id="4843a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4843a-113">-Context</span></span>
<span data-ttu-id="4843a-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="4843a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4843a-115">Aby uzyskać kontekst miejsca do magazynowania, New-AzStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4843a-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4843a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4843a-116">-DefaultProfile</span></span>
<span data-ttu-id="4843a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4843a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4843a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4843a-118">-Force</span></span>
<span data-ttu-id="4843a-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4843a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4843a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4843a-120">-Name</span></span>
<span data-ttu-id="4843a-121">Określa nazwę kolejki do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4843a-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4843a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4843a-122">-PassThru</span></span>
<span data-ttu-id="4843a-123">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="4843a-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4843a-124">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="4843a-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4843a-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4843a-125">-Confirm</span></span>
<span data-ttu-id="4843a-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4843a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4843a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4843a-127">-WhatIf</span></span>
<span data-ttu-id="4843a-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4843a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4843a-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4843a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4843a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4843a-130">CommonParameters</span></span>
<span data-ttu-id="4843a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4843a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4843a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4843a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4843a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4843a-133">INPUTS</span></span>

### <span data-ttu-id="4843a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4843a-134">System.String</span></span>

### <span data-ttu-id="4843a-135">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4843a-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4843a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4843a-136">OUTPUTS</span></span>

### <span data-ttu-id="4843a-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4843a-137">System.Boolean</span></span>

## <span data-ttu-id="4843a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4843a-138">NOTES</span></span>

## <span data-ttu-id="4843a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4843a-139">RELATED LINKS</span></span>

[<span data-ttu-id="4843a-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4843a-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="4843a-141">Nowe — AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4843a-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
