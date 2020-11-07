---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9c37421ff33bfb7f2a2308512e28fa8373ee308c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897521"
---
# <span data-ttu-id="d52ca-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d52ca-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d52ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d52ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d52ca-103">Usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d52ca-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d52ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d52ca-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d52ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d52ca-105">DESCRIPTION</span></span>
<span data-ttu-id="d52ca-106">Polecenie cmdlet **Remove-AzureStorageQueueStoredAccessPolicy** usuwa zapisane zasady dostępu z kolejki usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d52ca-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="d52ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d52ca-107">EXAMPLES</span></span>

### <span data-ttu-id="d52ca-108">Przykład 1: usuwanie zapisanych zasad dostępu z kolejki magazynu</span><span class="sxs-lookup"><span data-stu-id="d52ca-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="d52ca-109">To polecenie usuwa zasady dostępu o nazwie Policy04 z kolejki magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="d52ca-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="d52ca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d52ca-110">PARAMETERS</span></span>

### <span data-ttu-id="d52ca-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d52ca-111">-Context</span></span>
<span data-ttu-id="d52ca-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d52ca-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d52ca-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d52ca-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d52ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52ca-114">-DefaultProfile</span></span>
<span data-ttu-id="d52ca-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d52ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d52ca-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d52ca-116">-PassThru</span></span>
<span data-ttu-id="d52ca-117">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="d52ca-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d52ca-118">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="d52ca-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d52ca-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="d52ca-119">-Policy</span></span>
<span data-ttu-id="d52ca-120">Określa nazwę zasad dostępu przechowywanych, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d52ca-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d52ca-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="d52ca-121">-Queue</span></span>
<span data-ttu-id="d52ca-122">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d52ca-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d52ca-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d52ca-123">-Confirm</span></span>
<span data-ttu-id="d52ca-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d52ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d52ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d52ca-125">-WhatIf</span></span>
<span data-ttu-id="d52ca-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d52ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d52ca-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d52ca-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d52ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52ca-128">CommonParameters</span></span>
<span data-ttu-id="d52ca-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d52ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52ca-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d52ca-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52ca-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d52ca-131">INPUTS</span></span>

### <span data-ttu-id="d52ca-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d52ca-132">System.String</span></span>

### <span data-ttu-id="d52ca-133">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d52ca-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d52ca-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d52ca-134">OUTPUTS</span></span>

### <span data-ttu-id="d52ca-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d52ca-135">System.Boolean</span></span>

## <span data-ttu-id="d52ca-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d52ca-136">NOTES</span></span>

## <span data-ttu-id="d52ca-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d52ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="d52ca-138">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d52ca-138">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d52ca-139">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d52ca-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d52ca-140">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d52ca-140">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d52ca-141">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d52ca-141">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
