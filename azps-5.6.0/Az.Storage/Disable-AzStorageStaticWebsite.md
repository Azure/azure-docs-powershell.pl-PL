---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 12881d387d1e98bef8ca1fa00790b0332a338b7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973386"
---
# <span data-ttu-id="61feb-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="61feb-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="61feb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61feb-102">SYNOPSIS</span></span>
<span data-ttu-id="61feb-103">Wyłącz statyczną witrynę internetową dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61feb-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="61feb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61feb-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61feb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="61feb-105">DESCRIPTION</span></span>
<span data-ttu-id="61feb-106">Polecenie **cmdlet Disable-AzStorageWebsite** wyłącza statyczną witrynę internetową dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61feb-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="61feb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61feb-107">EXAMPLES</span></span>

### <span data-ttu-id="61feb-108">Przykład 1. Wyłączenie statycznej witryny sieci Web dla konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="61feb-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="61feb-109">To polecenie wyłącza statyczną witrynę internetową dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61feb-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="61feb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61feb-110">PARAMETERS</span></span>

### <span data-ttu-id="61feb-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="61feb-111">-Context</span></span>
<span data-ttu-id="61feb-112">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="61feb-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="61feb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61feb-113">-DefaultProfile</span></span>
<span data-ttu-id="61feb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61feb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61feb-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61feb-115">-PassThru</span></span>
<span data-ttu-id="61feb-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="61feb-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="61feb-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61feb-117">-Confirm</span></span>
<span data-ttu-id="61feb-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61feb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61feb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61feb-119">-WhatIf</span></span>
<span data-ttu-id="61feb-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61feb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61feb-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="61feb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61feb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61feb-122">CommonParameters</span></span>
<span data-ttu-id="61feb-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61feb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61feb-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61feb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61feb-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61feb-125">INPUTS</span></span>

### <span data-ttu-id="61feb-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="61feb-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="61feb-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61feb-127">OUTPUTS</span></span>

### <span data-ttu-id="61feb-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="61feb-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="61feb-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61feb-129">NOTES</span></span>

## <span data-ttu-id="61feb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61feb-130">RELATED LINKS</span></span>
