---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: dac884a0faf44380f19447f2d52af1e172feb9a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973393"
---
# <span data-ttu-id="e390c-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e390c-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e390c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e390c-102">SYNOPSIS</span></span>
<span data-ttu-id="e390c-103">Wyłącz zasady przechowywania usuwania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e390c-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e390c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e390c-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e390c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e390c-105">DESCRIPTION</span></span>
<span data-ttu-id="e390c-106">Polecenie cmdlet **Disable-AzStorageDeleteRetentionPolicy** wyłącza zasady przechowywania usuwania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e390c-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e390c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e390c-107">EXAMPLES</span></span>

### <span data-ttu-id="e390c-108">Przykład 1. Wyłączanie zasad przechowywania usuwania dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="e390c-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="e390c-109">To polecenie wyłącza zasady przechowywania usuwania dla usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="e390c-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="e390c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e390c-110">PARAMETERS</span></span>

### <span data-ttu-id="e390c-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e390c-111">-Context</span></span>
<span data-ttu-id="e390c-112">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e390c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e390c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e390c-113">-DefaultProfile</span></span>
<span data-ttu-id="e390c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e390c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e390c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e390c-115">-PassThru</span></span>
<span data-ttu-id="e390c-116">Wyświetlanie właściwości DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="e390c-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="e390c-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e390c-117">-Confirm</span></span>
<span data-ttu-id="e390c-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e390c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e390c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e390c-119">-WhatIf</span></span>
<span data-ttu-id="e390c-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e390c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e390c-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e390c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e390c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e390c-122">CommonParameters</span></span>
<span data-ttu-id="e390c-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e390c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e390c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e390c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e390c-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e390c-125">INPUTS</span></span>

### <span data-ttu-id="e390c-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e390c-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e390c-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e390c-127">OUTPUTS</span></span>

### <span data-ttu-id="e390c-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e390c-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e390c-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e390c-129">NOTES</span></span>

## <span data-ttu-id="e390c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e390c-130">RELATED LINKS</span></span>
