---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349813"
---
# <span data-ttu-id="27d61-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27d61-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="27d61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27d61-102">SYNOPSIS</span></span>
<span data-ttu-id="27d61-103">Wyłącz zasadę usuwania zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="27d61-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="27d61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27d61-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="27d61-105">DESCRIPTION</span></span>
<span data-ttu-id="27d61-106">Polecenie cmdlet **disable-AzStorageDeleteRetentionPolicy** wyłącza zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="27d61-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="27d61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27d61-107">EXAMPLES</span></span>

### <span data-ttu-id="27d61-108">Przykład 1. Wyłącz zasady usuwania zasad przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="27d61-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="27d61-109">To polecenie wyłącza zasady usuwania zasad przechowywania dla usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="27d61-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="27d61-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27d61-110">PARAMETERS</span></span>

### <span data-ttu-id="27d61-111">-Context</span><span class="sxs-lookup"><span data-stu-id="27d61-111">-Context</span></span>
<span data-ttu-id="27d61-112">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="27d61-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="27d61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d61-113">-DefaultProfile</span></span>
<span data-ttu-id="27d61-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27d61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27d61-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27d61-115">-PassThru</span></span>
<span data-ttu-id="27d61-116">Wyświetlanie DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="27d61-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="27d61-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27d61-117">-Confirm</span></span>
<span data-ttu-id="27d61-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27d61-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27d61-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d61-119">-WhatIf</span></span>
<span data-ttu-id="27d61-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27d61-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d61-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27d61-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27d61-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d61-122">CommonParameters</span></span>
<span data-ttu-id="27d61-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27d61-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d61-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27d61-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d61-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27d61-125">INPUTS</span></span>

### <span data-ttu-id="27d61-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="27d61-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="27d61-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27d61-127">OUTPUTS</span></span>

### <span data-ttu-id="27d61-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27d61-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="27d61-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27d61-129">NOTES</span></span>

## <span data-ttu-id="27d61-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27d61-130">RELATED LINKS</span></span>
