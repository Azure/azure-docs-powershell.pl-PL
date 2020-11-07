---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d899b34e2f880a0351ce4d10f360f7bc29011b0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898610"
---
# <span data-ttu-id="a2717-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a2717-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a2717-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2717-102">SYNOPSIS</span></span>
<span data-ttu-id="a2717-103">Wyłącz zasadę usuwania zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="a2717-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2717-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2717-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2717-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2717-105">DESCRIPTION</span></span>
<span data-ttu-id="a2717-106">Polecenie cmdlet **disable-AzureStorageDeleteRetentionPolicy** wyłącza zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a2717-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="a2717-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2717-107">EXAMPLES</span></span>

### <span data-ttu-id="a2717-108">Przykład 1. Wyłącz zasady usuwania zasad przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="a2717-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="a2717-109">To polecenie wyłącza zasady usuwania zasad przechowywania dla usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="a2717-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="a2717-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2717-110">PARAMETERS</span></span>

### <span data-ttu-id="a2717-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a2717-111">-Context</span></span>
<span data-ttu-id="a2717-112">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="a2717-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a2717-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2717-113">-DefaultProfile</span></span>
<span data-ttu-id="a2717-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2717-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2717-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2717-115">-PassThru</span></span>
<span data-ttu-id="a2717-116">Wyświetlanie DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="a2717-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="a2717-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2717-117">-Confirm</span></span>
<span data-ttu-id="a2717-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2717-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2717-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2717-119">-WhatIf</span></span>
<span data-ttu-id="a2717-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2717-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2717-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2717-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2717-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2717-122">CommonParameters</span></span>
<span data-ttu-id="a2717-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2717-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2717-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2717-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2717-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2717-125">INPUTS</span></span>

### <span data-ttu-id="a2717-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2717-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a2717-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2717-127">OUTPUTS</span></span>

### <span data-ttu-id="a2717-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a2717-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a2717-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2717-129">NOTES</span></span>

## <span data-ttu-id="a2717-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2717-130">RELATED LINKS</span></span>
