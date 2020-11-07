---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2afb39aafacef354c4e50aad1ce0a4824622c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707533"
---
# <span data-ttu-id="a9074-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a9074-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="a9074-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9074-102">SYNOPSIS</span></span>
<span data-ttu-id="a9074-103">Usuwa kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="a9074-103">Removes a storage queue.</span></span>

## <span data-ttu-id="a9074-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9074-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9074-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9074-105">DESCRIPTION</span></span>
<span data-ttu-id="a9074-106">Polecenie cmdlet **Remove-AzStorageQueue** umożliwia usunięcie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="a9074-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="a9074-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9074-107">EXAMPLES</span></span>

### <span data-ttu-id="a9074-108">Przykład 1: usuwanie kolejki magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="a9074-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="a9074-109">To polecenie umożliwia usunięcie kolejki o nazwie ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="a9074-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="a9074-110">Przykład 2: usuwanie wielu kolejek magazynowania</span><span class="sxs-lookup"><span data-stu-id="a9074-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="a9074-111">To polecenie usuwa wszystkie kolejki o nazwach rozpoczynających się od contoso.</span><span class="sxs-lookup"><span data-stu-id="a9074-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="a9074-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9074-112">PARAMETERS</span></span>

### <span data-ttu-id="a9074-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a9074-113">-Context</span></span>
<span data-ttu-id="a9074-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a9074-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a9074-115">Aby uzyskać kontekst miejsca do magazynowania, New-AzStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9074-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a9074-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9074-116">-DefaultProfile</span></span>
<span data-ttu-id="a9074-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9074-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9074-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a9074-118">-Force</span></span>
<span data-ttu-id="a9074-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9074-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9074-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9074-120">-Name</span></span>
<span data-ttu-id="a9074-121">Określa nazwę kolejki do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a9074-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="a9074-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9074-122">-PassThru</span></span>
<span data-ttu-id="a9074-123">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="a9074-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a9074-124">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="a9074-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a9074-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9074-125">-Confirm</span></span>
<span data-ttu-id="a9074-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9074-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9074-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9074-127">-WhatIf</span></span>
<span data-ttu-id="a9074-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9074-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9074-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9074-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9074-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9074-130">CommonParameters</span></span>
<span data-ttu-id="a9074-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9074-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9074-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9074-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9074-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9074-133">INPUTS</span></span>

### <span data-ttu-id="a9074-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a9074-134">System.String</span></span>

### <span data-ttu-id="a9074-135">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9074-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9074-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9074-136">OUTPUTS</span></span>

### <span data-ttu-id="a9074-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9074-137">System.Boolean</span></span>

## <span data-ttu-id="a9074-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9074-138">NOTES</span></span>

## <span data-ttu-id="a9074-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9074-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9074-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a9074-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="a9074-141">Nowe — AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a9074-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
