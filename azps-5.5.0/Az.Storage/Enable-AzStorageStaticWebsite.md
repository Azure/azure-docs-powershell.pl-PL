---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198491"
---
# <span data-ttu-id="53302-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="53302-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="53302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53302-102">SYNOPSIS</span></span>
<span data-ttu-id="53302-103">Włącz statyczną witrynę internetową dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53302-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="53302-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53302-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53302-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="53302-105">DESCRIPTION</span></span>
<span data-ttu-id="53302-106">Polecenie **cmdlet Enable-AzStorageWebsite** umożliwia obsługę statycznej witryny internetowej dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53302-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="53302-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53302-107">EXAMPLES</span></span>

### <span data-ttu-id="53302-108">Przykład 1. Włączanie statycznej witryny internetowej dla konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="53302-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="53302-109">To polecenie włącza statyczną witrynę internetową dla konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53302-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="53302-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53302-110">PARAMETERS</span></span>

### <span data-ttu-id="53302-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="53302-111">-Context</span></span>
<span data-ttu-id="53302-112">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="53302-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="53302-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53302-113">-DefaultProfile</span></span>
<span data-ttu-id="53302-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="53302-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53302-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="53302-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="53302-116">Ścieżka do dokumentu błędu, która powinna być wyświetlana po wystawiu 404 (co oznacza, że przeglądarka żąda strony, która nie istnieje).</span><span class="sxs-lookup"><span data-stu-id="53302-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53302-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="53302-117">-IndexDocument</span></span>
<span data-ttu-id="53302-118">Nazwa dokumentu indeksu w każdym katalogu.</span><span class="sxs-lookup"><span data-stu-id="53302-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53302-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53302-119">-PassThru</span></span>
<span data-ttu-id="53302-120">Ustawienie Wyświetlania statycznej witryny sieci Web w właściwościach usługi.</span><span class="sxs-lookup"><span data-stu-id="53302-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="53302-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53302-121">-Confirm</span></span>
<span data-ttu-id="53302-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="53302-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53302-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53302-123">-WhatIf</span></span>
<span data-ttu-id="53302-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53302-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53302-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="53302-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53302-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53302-126">CommonParameters</span></span>
<span data-ttu-id="53302-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53302-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53302-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53302-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53302-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53302-129">INPUTS</span></span>

### <span data-ttu-id="53302-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="53302-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="53302-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53302-131">OUTPUTS</span></span>

### <span data-ttu-id="53302-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="53302-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="53302-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53302-133">NOTES</span></span>

## <span data-ttu-id="53302-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53302-134">RELATED LINKS</span></span>
