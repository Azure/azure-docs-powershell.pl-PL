---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523909"
---
# <span data-ttu-id="56597-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56597-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="56597-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56597-102">SYNOPSIS</span></span>
<span data-ttu-id="56597-103">Usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="56597-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="56597-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56597-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56597-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56597-105">DESCRIPTION</span></span>
<span data-ttu-id="56597-106">Polecenie cmdlet **Remove-AzureStorageQueueStoredAccessPolicy** usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="56597-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="56597-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56597-107">EXAMPLES</span></span>

### <span data-ttu-id="56597-108">Przykład 1: usuwanie zapisanych zasad dostępu z kolejki magazynu</span><span class="sxs-lookup"><span data-stu-id="56597-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="56597-109">To polecenie usuwa zasady dostępu o nazwie Policy04 z kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="56597-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="56597-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56597-110">PARAMETERS</span></span>

### <span data-ttu-id="56597-111">-Context</span><span class="sxs-lookup"><span data-stu-id="56597-111">-Context</span></span>
<span data-ttu-id="56597-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="56597-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="56597-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="56597-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56597-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56597-114">-PassThru</span></span>
<span data-ttu-id="56597-115">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="56597-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="56597-116">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="56597-116">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56597-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="56597-117">-Policy</span></span>
<span data-ttu-id="56597-118">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="56597-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="56597-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="56597-119">-Queue</span></span>
<span data-ttu-id="56597-120">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56597-120">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56597-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56597-121">-Confirm</span></span>
<span data-ttu-id="56597-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56597-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56597-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56597-123">-WhatIf</span></span>
<span data-ttu-id="56597-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56597-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56597-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56597-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56597-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56597-126">CommonParameters</span></span>
<span data-ttu-id="56597-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56597-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56597-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56597-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56597-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56597-129">INPUTS</span></span>

## <span data-ttu-id="56597-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56597-130">OUTPUTS</span></span>

## <span data-ttu-id="56597-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56597-131">NOTES</span></span>

## <span data-ttu-id="56597-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56597-132">RELATED LINKS</span></span>

[<span data-ttu-id="56597-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56597-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="56597-134">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="56597-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="56597-135">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56597-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="56597-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="56597-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
