---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: e2fcfa1d100f460bcf352cc26fd0e094d52cad21
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898565"
---
# <span data-ttu-id="5ee79-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5ee79-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="5ee79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ee79-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee79-103">Usuwa kolejkę magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ee79-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ee79-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee79-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ee79-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee79-106">Polecenie cmdlet **Remove-AzureStorageQueue** umożliwia usunięcie kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="5ee79-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="5ee79-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ee79-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee79-108">Przykład 1: usuwanie kolejki magazynu według nazwy</span><span class="sxs-lookup"><span data-stu-id="5ee79-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="5ee79-109">To polecenie umożliwia usunięcie kolejki o nazwie ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="5ee79-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="5ee79-110">Przykład 2: usuwanie wielu kolejek magazynowania</span><span class="sxs-lookup"><span data-stu-id="5ee79-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="5ee79-111">To polecenie usuwa wszystkie kolejki o nazwach rozpoczynających się od contoso.</span><span class="sxs-lookup"><span data-stu-id="5ee79-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="5ee79-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ee79-112">PARAMETERS</span></span>

### <span data-ttu-id="5ee79-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5ee79-113">-Context</span></span>
<span data-ttu-id="5ee79-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5ee79-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5ee79-115">Aby uzyskać kontekst miejsca do magazynowania, New-AzureStorageContext polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee79-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5ee79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee79-116">-DefaultProfile</span></span>
<span data-ttu-id="5ee79-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee79-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ee79-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5ee79-118">-Force</span></span>
<span data-ttu-id="5ee79-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5ee79-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ee79-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ee79-120">-Name</span></span>
<span data-ttu-id="5ee79-121">Określa nazwę kolejki do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5ee79-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="5ee79-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ee79-122">-PassThru</span></span>
<span data-ttu-id="5ee79-123">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="5ee79-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5ee79-124">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="5ee79-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5ee79-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ee79-125">-Confirm</span></span>
<span data-ttu-id="5ee79-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee79-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee79-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee79-127">-WhatIf</span></span>
<span data-ttu-id="5ee79-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ee79-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee79-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ee79-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee79-130">CommonParameters</span></span>
<span data-ttu-id="5ee79-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee79-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee79-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee79-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ee79-133">INPUTS</span></span>

### <span data-ttu-id="5ee79-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee79-134">System.String</span></span>

### <span data-ttu-id="5ee79-135">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ee79-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5ee79-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ee79-136">OUTPUTS</span></span>

### <span data-ttu-id="5ee79-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ee79-137">System.Boolean</span></span>

## <span data-ttu-id="5ee79-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ee79-138">NOTES</span></span>

## <span data-ttu-id="5ee79-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ee79-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ee79-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5ee79-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="5ee79-141">Nowe — AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5ee79-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
