---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198411"
---
# <span data-ttu-id="39847-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="39847-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="39847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39847-102">SYNOPSIS</span></span>
<span data-ttu-id="39847-103">Usuwa kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="39847-103">Removes a storage queue.</span></span>

## <span data-ttu-id="39847-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39847-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39847-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39847-105">DESCRIPTION</span></span>
<span data-ttu-id="39847-106">Polecenie **cmdlet Remove-AzStorageQueue** usuwa kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="39847-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="39847-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39847-107">EXAMPLES</span></span>

### <span data-ttu-id="39847-108">Przykład 1. Usuwanie kolejki magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="39847-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="39847-109">To polecenie usuwa kolejkę o nazwie ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="39847-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="39847-110">Przykład 2. Usuwanie wielu kolejek magazynu</span><span class="sxs-lookup"><span data-stu-id="39847-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="39847-111">To polecenie usuwa wszystkie kolejki z nazwami, które zaczynają się od nazwy Contoso.</span><span class="sxs-lookup"><span data-stu-id="39847-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="39847-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39847-112">PARAMETERS</span></span>

### <span data-ttu-id="39847-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="39847-113">-Context</span></span>
<span data-ttu-id="39847-114">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="39847-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="39847-115">Aby uzyskać kontekst magazynowania, New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39847-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="39847-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39847-116">-DefaultProfile</span></span>
<span data-ttu-id="39847-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="39847-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39847-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="39847-118">-Force</span></span>
<span data-ttu-id="39847-119">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="39847-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="39847-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="39847-120">-Name</span></span>
<span data-ttu-id="39847-121">Określa nazwę kolejki do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="39847-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="39847-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39847-122">-PassThru</span></span>
<span data-ttu-id="39847-123">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="39847-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="39847-124">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="39847-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="39847-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39847-125">-Confirm</span></span>
<span data-ttu-id="39847-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39847-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39847-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39847-127">-WhatIf</span></span>
<span data-ttu-id="39847-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39847-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39847-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="39847-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39847-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39847-130">CommonParameters</span></span>
<span data-ttu-id="39847-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39847-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39847-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39847-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39847-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39847-133">INPUTS</span></span>

### <span data-ttu-id="39847-134">System.String</span><span class="sxs-lookup"><span data-stu-id="39847-134">System.String</span></span>

### <span data-ttu-id="39847-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="39847-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="39847-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39847-136">OUTPUTS</span></span>

### <span data-ttu-id="39847-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39847-137">System.Boolean</span></span>

## <span data-ttu-id="39847-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39847-138">NOTES</span></span>

## <span data-ttu-id="39847-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39847-139">RELATED LINKS</span></span>

[<span data-ttu-id="39847-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="39847-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="39847-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="39847-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
