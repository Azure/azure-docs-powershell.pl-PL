---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b1e06a31cfbe16cb04a7158cd62858683db6e131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542083"
---
# <span data-ttu-id="65d90-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65d90-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="65d90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65d90-102">SYNOPSIS</span></span>
<span data-ttu-id="65d90-103">Usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65d90-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65d90-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65d90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65d90-105">DESCRIPTION</span></span>
<span data-ttu-id="65d90-106">Polecenie cmdlet **Remove-AzureStorageTableStoredAccessPolicy** usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65d90-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="65d90-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65d90-107">EXAMPLES</span></span>

### <span data-ttu-id="65d90-108">Przykład 1: usuwanie zapisanych zasad dostępu z tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="65d90-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="65d90-109">To polecenie usuwa zasady o nazwie Policy05 z tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="65d90-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="65d90-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65d90-110">PARAMETERS</span></span>

### <span data-ttu-id="65d90-111">-Context</span><span class="sxs-lookup"><span data-stu-id="65d90-111">-Context</span></span>
<span data-ttu-id="65d90-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="65d90-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="65d90-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="65d90-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="65d90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d90-114">-DefaultProfile</span></span>
<span data-ttu-id="65d90-115">Komunikacja z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65d90-115">communication with Azure.</span></span>

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

### <span data-ttu-id="65d90-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65d90-116">-PassThru</span></span>
<span data-ttu-id="65d90-117">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="65d90-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="65d90-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="65d90-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="65d90-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="65d90-119">-Policy</span></span>
<span data-ttu-id="65d90-120">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d90-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="65d90-121">-Table</span><span class="sxs-lookup"><span data-stu-id="65d90-121">-Table</span></span>
<span data-ttu-id="65d90-122">Określa nazwę tabeli platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65d90-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="65d90-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65d90-123">-Confirm</span></span>
<span data-ttu-id="65d90-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d90-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d90-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d90-125">-WhatIf</span></span>
<span data-ttu-id="65d90-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d90-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d90-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65d90-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d90-128">CommonParameters</span></span>
<span data-ttu-id="65d90-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d90-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d90-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65d90-131">INPUTS</span></span>

### <span data-ttu-id="65d90-132">System. String</span><span class="sxs-lookup"><span data-stu-id="65d90-132">System.String</span></span>

### <span data-ttu-id="65d90-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="65d90-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="65d90-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65d90-134">OUTPUTS</span></span>

### <span data-ttu-id="65d90-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65d90-135">System.Boolean</span></span>

## <span data-ttu-id="65d90-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65d90-136">NOTES</span></span>

## <span data-ttu-id="65d90-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65d90-137">RELATED LINKS</span></span>

[<span data-ttu-id="65d90-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65d90-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="65d90-139">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="65d90-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="65d90-140">Nowe — AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65d90-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="65d90-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="65d90-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
