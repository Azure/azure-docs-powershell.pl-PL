---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195826"
---
# <span data-ttu-id="76a62-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76a62-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="76a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a62-102">SYNOPSIS</span></span>
<span data-ttu-id="76a62-103">Włącz zasady przechowywania usuwania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76a62-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="76a62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76a62-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a62-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76a62-105">DESCRIPTION</span></span>
<span data-ttu-id="76a62-106">Polecenie **cmdlet Enable-AzStorageDeleteRetentionPolicy** umożliwia usuwanie zasad przechowywania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="76a62-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="76a62-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76a62-107">EXAMPLES</span></span>

### <span data-ttu-id="76a62-108">Przykład 1. Włączanie zasad przechowywania usuwania dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="76a62-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="76a62-109">To polecenie umożliwia usuwanie zasad przechowywania dla usługi obiektów blob i ustawianie dni przechowywania usuniętych obiektów blob na 3.</span><span class="sxs-lookup"><span data-stu-id="76a62-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="76a62-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76a62-110">PARAMETERS</span></span>

### <span data-ttu-id="76a62-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="76a62-111">-Context</span></span>
<span data-ttu-id="76a62-112">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="76a62-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="76a62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a62-113">-DefaultProfile</span></span>
<span data-ttu-id="76a62-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76a62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a62-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76a62-115">-PassThru</span></span>
<span data-ttu-id="76a62-116">Wyświetlanie właściwości DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="76a62-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="76a62-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="76a62-117">-RetentionDays</span></span>
<span data-ttu-id="76a62-118">Ustawia liczbę dni przechowywania dla wartości DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="76a62-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a62-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76a62-119">-Confirm</span></span>
<span data-ttu-id="76a62-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76a62-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a62-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a62-121">-WhatIf</span></span>
<span data-ttu-id="76a62-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76a62-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a62-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="76a62-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a62-124">CommonParameters</span></span>
<span data-ttu-id="76a62-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a62-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a62-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a62-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76a62-127">INPUTS</span></span>

### <span data-ttu-id="76a62-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="76a62-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="76a62-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76a62-129">OUTPUTS</span></span>

### <span data-ttu-id="76a62-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="76a62-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="76a62-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76a62-131">NOTES</span></span>

## <span data-ttu-id="76a62-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76a62-132">RELATED LINKS</span></span>
