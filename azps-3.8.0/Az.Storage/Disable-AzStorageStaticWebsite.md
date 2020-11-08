---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050219"
---
# <span data-ttu-id="5ffea-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5ffea-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="5ffea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ffea-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffea-103">Wyłącz statyczną witrynę sieci Web dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5ffea-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="5ffea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ffea-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ffea-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffea-106">Polecenie cmdlet **disable-AzStorageStaticWebsite** wyłącza statyczną witrynę sieci Web dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5ffea-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="5ffea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ffea-107">EXAMPLES</span></span>

### <span data-ttu-id="5ffea-108">Przykład 1: wyłączanie statycznej witryny sieci Web dla konta usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="5ffea-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="5ffea-109">To polecenie wyłącza statyczną witrynę sieci Web dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="5ffea-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="5ffea-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ffea-110">PARAMETERS</span></span>

### <span data-ttu-id="5ffea-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5ffea-111">-Context</span></span>
<span data-ttu-id="5ffea-112">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="5ffea-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="5ffea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffea-113">-DefaultProfile</span></span>
<span data-ttu-id="5ffea-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ffea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ffea-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ffea-115">-PassThru</span></span>
<span data-ttu-id="5ffea-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ffea-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5ffea-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ffea-117">-Confirm</span></span>
<span data-ttu-id="5ffea-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ffea-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffea-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffea-119">-WhatIf</span></span>
<span data-ttu-id="5ffea-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ffea-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ffea-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ffea-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffea-122">CommonParameters</span></span>
<span data-ttu-id="5ffea-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffea-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ffea-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffea-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ffea-125">INPUTS</span></span>

### <span data-ttu-id="5ffea-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ffea-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5ffea-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ffea-127">OUTPUTS</span></span>

### <span data-ttu-id="5ffea-128">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="5ffea-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="5ffea-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ffea-129">NOTES</span></span>

## <span data-ttu-id="5ffea-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ffea-130">RELATED LINKS</span></span>
