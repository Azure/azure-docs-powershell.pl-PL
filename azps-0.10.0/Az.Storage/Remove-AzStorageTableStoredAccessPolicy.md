---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 96c6d80f4281b8d3e10d29a288787ff9ebcc5586
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892062"
---
# <span data-ttu-id="d0222-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0222-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d0222-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0222-102">SYNOPSIS</span></span>
<span data-ttu-id="d0222-103">Usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0222-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="d0222-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0222-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0222-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0222-105">DESCRIPTION</span></span>
<span data-ttu-id="d0222-106">Polecenie cmdlet **Remove-AzStorageTableStoredAccessPolicy** usuwa zapisane zasady dostępu z tabeli magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0222-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="d0222-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0222-107">EXAMPLES</span></span>

### <span data-ttu-id="d0222-108">Przykład 1: usuwanie zapisanych zasad dostępu z tabeli magazynu</span><span class="sxs-lookup"><span data-stu-id="d0222-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="d0222-109">To polecenie usuwa zasady o nazwie Policy05 z tabeli magazynu o nazwie MyTable.</span><span class="sxs-lookup"><span data-stu-id="d0222-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="d0222-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0222-110">PARAMETERS</span></span>

### <span data-ttu-id="d0222-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d0222-111">-Context</span></span>
<span data-ttu-id="d0222-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d0222-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d0222-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d0222-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d0222-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0222-114">-DefaultProfile</span></span>
<span data-ttu-id="d0222-115">Komunikacja z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0222-115">communication with Azure.</span></span>

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

### <span data-ttu-id="d0222-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0222-116">-PassThru</span></span>
<span data-ttu-id="d0222-117">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="d0222-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d0222-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="d0222-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d0222-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="d0222-119">-Policy</span></span>
<span data-ttu-id="d0222-120">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0222-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0222-121">-Table</span><span class="sxs-lookup"><span data-stu-id="d0222-121">-Table</span></span>
<span data-ttu-id="d0222-122">Określa nazwę tabeli platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0222-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="d0222-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0222-123">-Confirm</span></span>
<span data-ttu-id="d0222-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0222-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0222-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0222-125">-WhatIf</span></span>
<span data-ttu-id="d0222-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0222-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0222-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0222-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0222-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0222-128">CommonParameters</span></span>
<span data-ttu-id="d0222-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0222-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0222-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0222-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0222-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0222-131">INPUTS</span></span>

### <span data-ttu-id="d0222-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d0222-132">System.String</span></span>

### <span data-ttu-id="d0222-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0222-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d0222-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0222-134">OUTPUTS</span></span>

### <span data-ttu-id="d0222-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0222-135">System.Boolean</span></span>

## <span data-ttu-id="d0222-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0222-136">NOTES</span></span>

## <span data-ttu-id="d0222-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0222-137">RELATED LINKS</span></span>

[<span data-ttu-id="d0222-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0222-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d0222-139">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0222-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d0222-140">Nowe — AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0222-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d0222-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0222-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
