---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 76f36fa6cc7b2ab51604f59fb40170734f5ce99f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707523"
---
# <span data-ttu-id="69931-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69931-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="69931-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69931-102">SYNOPSIS</span></span>
<span data-ttu-id="69931-103">Usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69931-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="69931-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69931-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69931-105">Opis</span><span class="sxs-lookup"><span data-stu-id="69931-105">DESCRIPTION</span></span>
<span data-ttu-id="69931-106">Polecenie cmdlet **Remove-AzStorageTableStoredAccessPolicy** usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69931-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="69931-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69931-107">EXAMPLES</span></span>

### <span data-ttu-id="69931-108">Przykład 1: usuwanie zapisanych zasad dostępu z tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="69931-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="69931-109">To polecenie usuwa zasady o nazwie Policy05 z tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="69931-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="69931-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69931-110">PARAMETERS</span></span>

### <span data-ttu-id="69931-111">-Context</span><span class="sxs-lookup"><span data-stu-id="69931-111">-Context</span></span>
<span data-ttu-id="69931-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="69931-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="69931-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="69931-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="69931-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69931-114">-DefaultProfile</span></span>
<span data-ttu-id="69931-115">Komunikacja z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69931-115">communication with Azure.</span></span>

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

### <span data-ttu-id="69931-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69931-116">-PassThru</span></span>
<span data-ttu-id="69931-117">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="69931-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="69931-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="69931-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="69931-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="69931-119">-Policy</span></span>
<span data-ttu-id="69931-120">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69931-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="69931-121">-Table</span><span class="sxs-lookup"><span data-stu-id="69931-121">-Table</span></span>
<span data-ttu-id="69931-122">Określa nazwę tabeli platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69931-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="69931-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69931-123">-Confirm</span></span>
<span data-ttu-id="69931-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69931-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69931-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69931-125">-WhatIf</span></span>
<span data-ttu-id="69931-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69931-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69931-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69931-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69931-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69931-128">CommonParameters</span></span>
<span data-ttu-id="69931-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69931-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69931-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69931-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69931-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69931-131">INPUTS</span></span>

### <span data-ttu-id="69931-132">System. String</span><span class="sxs-lookup"><span data-stu-id="69931-132">System.String</span></span>

### <span data-ttu-id="69931-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="69931-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="69931-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69931-134">OUTPUTS</span></span>

### <span data-ttu-id="69931-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69931-135">System.Boolean</span></span>

## <span data-ttu-id="69931-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69931-136">NOTES</span></span>

## <span data-ttu-id="69931-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69931-137">RELATED LINKS</span></span>

[<span data-ttu-id="69931-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69931-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="69931-139">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="69931-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="69931-140">Nowe — AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69931-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="69931-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69931-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
