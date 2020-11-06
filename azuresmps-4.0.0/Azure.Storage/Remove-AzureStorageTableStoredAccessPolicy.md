---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523225"
---
# <span data-ttu-id="30322-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30322-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="30322-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30322-102">SYNOPSIS</span></span>
<span data-ttu-id="30322-103">Usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="30322-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="30322-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30322-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30322-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30322-105">DESCRIPTION</span></span>
<span data-ttu-id="30322-106">Polecenie cmdlet **Remove-AzureStorageTableStoredAccessPolicy** usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="30322-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="30322-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30322-107">EXAMPLES</span></span>

### <span data-ttu-id="30322-108">Przykład 1: usuwanie zapisanych zasad dostępu z tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="30322-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="30322-109">To polecenie usuwa zasady o nazwie Policy05 z tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="30322-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="30322-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30322-110">PARAMETERS</span></span>

### <span data-ttu-id="30322-111">-Context</span><span class="sxs-lookup"><span data-stu-id="30322-111">-Context</span></span>
<span data-ttu-id="30322-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="30322-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="30322-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="30322-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="30322-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30322-114">-PassThru</span></span>
<span data-ttu-id="30322-115">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="30322-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="30322-116">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="30322-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="30322-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="30322-117">-Policy</span></span>
<span data-ttu-id="30322-118">Określa przechowywane zasady dostępu, które zawierają uprawnienia dla tego tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="30322-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="30322-119">-Table</span><span class="sxs-lookup"><span data-stu-id="30322-119">-Table</span></span>
<span data-ttu-id="30322-120">Określa nazwę tabeli platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="30322-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="30322-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30322-121">-Confirm</span></span>
<span data-ttu-id="30322-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30322-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30322-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30322-123">-WhatIf</span></span>
<span data-ttu-id="30322-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30322-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30322-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30322-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30322-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30322-126">CommonParameters</span></span>
<span data-ttu-id="30322-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30322-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30322-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30322-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30322-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30322-129">INPUTS</span></span>

## <span data-ttu-id="30322-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30322-130">OUTPUTS</span></span>

## <span data-ttu-id="30322-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30322-131">NOTES</span></span>

## <span data-ttu-id="30322-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30322-132">RELATED LINKS</span></span>

[<span data-ttu-id="30322-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30322-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="30322-134">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="30322-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="30322-135">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30322-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="30322-136">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30322-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
