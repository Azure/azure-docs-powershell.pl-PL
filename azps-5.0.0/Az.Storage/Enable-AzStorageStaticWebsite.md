---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224985"
---
# <span data-ttu-id="08595-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08595-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="08595-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08595-102">SYNOPSIS</span></span>
<span data-ttu-id="08595-103">Włącz statyczną witrynę sieci Web dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="08595-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="08595-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08595-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08595-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08595-105">DESCRIPTION</span></span>
<span data-ttu-id="08595-106">Polecenie cmdlet **enable-AzStorageStaticWebsite** włącza statyczną witrynę sieci Web dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="08595-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="08595-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08595-107">EXAMPLES</span></span>

### <span data-ttu-id="08595-108">Przykład 1: Włączanie statycznej witryny sieci Web dla konta usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="08595-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="08595-109">To polecenie umożliwia włączenie statycznej witryny sieci Web dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="08595-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="08595-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08595-110">PARAMETERS</span></span>

### <span data-ttu-id="08595-111">-Context</span><span class="sxs-lookup"><span data-stu-id="08595-111">-Context</span></span>
<span data-ttu-id="08595-112">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="08595-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="08595-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08595-113">-DefaultProfile</span></span>
<span data-ttu-id="08595-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08595-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08595-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="08595-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="08595-116">Ścieżka do dokumentu o błędzie, który powinien być wyświetlany po wygenerowaniu 404 (znaczenie, gdy przeglądarka żąda strony, która nie istnieje).</span><span class="sxs-lookup"><span data-stu-id="08595-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="08595-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="08595-117">-IndexDocument</span></span>
<span data-ttu-id="08595-118">Nazwa dokumentu indeksu w każdym katalogu.</span><span class="sxs-lookup"><span data-stu-id="08595-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="08595-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08595-119">-PassThru</span></span>
<span data-ttu-id="08595-120">Wyświetlanie ustawienia statycznej witryny sieci Web w witrynie serviceproperties.</span><span class="sxs-lookup"><span data-stu-id="08595-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="08595-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08595-121">-Confirm</span></span>
<span data-ttu-id="08595-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08595-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08595-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08595-123">-WhatIf</span></span>
<span data-ttu-id="08595-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08595-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08595-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08595-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08595-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08595-126">CommonParameters</span></span>
<span data-ttu-id="08595-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08595-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08595-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08595-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08595-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08595-129">INPUTS</span></span>

### <span data-ttu-id="08595-130">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="08595-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="08595-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08595-131">OUTPUTS</span></span>

### <span data-ttu-id="08595-132">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="08595-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="08595-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08595-133">NOTES</span></span>

## <span data-ttu-id="08595-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08595-134">RELATED LINKS</span></span>
