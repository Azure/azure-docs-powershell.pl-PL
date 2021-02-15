---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190914"
---
# <span data-ttu-id="881de-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="881de-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="881de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="881de-102">SYNOPSIS</span></span>
<span data-ttu-id="881de-103">Wyłącz zasady przechowywania usuwania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="881de-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="881de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="881de-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="881de-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="881de-105">DESCRIPTION</span></span>
<span data-ttu-id="881de-106">Polecenie cmdlet **Disable-AzStorageDeleteRetentionPolicy** wyłącza zasady przechowywania usuwania dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="881de-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="881de-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="881de-107">EXAMPLES</span></span>

### <span data-ttu-id="881de-108">Przykład 1. Wyłączanie zasad przechowywania usuwania dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="881de-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="881de-109">To polecenie wyłącza zasady przechowywania usuwania dla usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="881de-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="881de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="881de-110">PARAMETERS</span></span>

### <span data-ttu-id="881de-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="881de-111">-Context</span></span>
<span data-ttu-id="881de-112">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="881de-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="881de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="881de-113">-DefaultProfile</span></span>
<span data-ttu-id="881de-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="881de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="881de-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="881de-115">-PassThru</span></span>
<span data-ttu-id="881de-116">Wyświetlanie właściwości DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="881de-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="881de-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="881de-117">-Confirm</span></span>
<span data-ttu-id="881de-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="881de-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="881de-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="881de-119">-WhatIf</span></span>
<span data-ttu-id="881de-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="881de-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="881de-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="881de-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="881de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="881de-122">CommonParameters</span></span>
<span data-ttu-id="881de-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="881de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="881de-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="881de-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="881de-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="881de-125">INPUTS</span></span>

### <span data-ttu-id="881de-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="881de-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="881de-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="881de-127">OUTPUTS</span></span>

### <span data-ttu-id="881de-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="881de-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="881de-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="881de-129">NOTES</span></span>

## <span data-ttu-id="881de-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="881de-130">RELATED LINKS</span></span>
