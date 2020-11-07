---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6d32ddf53f675f2ab2897e4bb9ec85655e0fcd14
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899160"
---
# <span data-ttu-id="fb929-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fb929-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="fb929-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb929-102">SYNOPSIS</span></span>
<span data-ttu-id="fb929-103">Usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb929-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb929-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb929-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb929-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb929-105">DESCRIPTION</span></span>
<span data-ttu-id="fb929-106">Polecenie cmdlet **Remove-AzureStorageTableStoredAccessPolicy** usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb929-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="fb929-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb929-107">EXAMPLES</span></span>

### <span data-ttu-id="fb929-108">Przykład 1: usuwanie zapisanych zasad dostępu z tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="fb929-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="fb929-109">To polecenie usuwa zasady o nazwie Policy05 z tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="fb929-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="fb929-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb929-110">PARAMETERS</span></span>

### <span data-ttu-id="fb929-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fb929-111">-Context</span></span>
<span data-ttu-id="fb929-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="fb929-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fb929-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fb929-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fb929-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb929-114">-DefaultProfile</span></span>
<span data-ttu-id="fb929-115">Komunikacja z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb929-115">communication with Azure.</span></span>

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

### <span data-ttu-id="fb929-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb929-116">-PassThru</span></span>
<span data-ttu-id="fb929-117">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="fb929-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fb929-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="fb929-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fb929-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="fb929-119">-Policy</span></span>
<span data-ttu-id="fb929-120">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb929-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fb929-121">-Table</span><span class="sxs-lookup"><span data-stu-id="fb929-121">-Table</span></span>
<span data-ttu-id="fb929-122">Określa nazwę tabeli platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb929-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="fb929-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb929-123">-Confirm</span></span>
<span data-ttu-id="fb929-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb929-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb929-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb929-125">-WhatIf</span></span>
<span data-ttu-id="fb929-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb929-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb929-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb929-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb929-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb929-128">CommonParameters</span></span>
<span data-ttu-id="fb929-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb929-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb929-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb929-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb929-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb929-131">INPUTS</span></span>

### <span data-ttu-id="fb929-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fb929-132">System.String</span></span>

### <span data-ttu-id="fb929-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fb929-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fb929-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb929-134">OUTPUTS</span></span>

### <span data-ttu-id="fb929-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb929-135">System.Boolean</span></span>

## <span data-ttu-id="fb929-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb929-136">NOTES</span></span>

## <span data-ttu-id="fb929-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb929-137">RELATED LINKS</span></span>

[<span data-ttu-id="fb929-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fb929-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fb929-139">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fb929-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fb929-140">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fb929-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fb929-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fb929-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
