---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: e9825c0efe0f54788cb074c862d51b747c6fbb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887201"
---
# <span data-ttu-id="a7300-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7300-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a7300-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7300-102">SYNOPSIS</span></span>
<span data-ttu-id="a7300-103">Włącz zasady dotyczące przechowywania obiektów BLOB usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a7300-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="a7300-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7300-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7300-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7300-105">DESCRIPTION</span></span>
<span data-ttu-id="a7300-106">Polecenie cmdlet **enable-AzStorageDeleteRetentionPolicy** umożliwia usuwanie zasad przechowywania dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="a7300-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="a7300-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7300-107">EXAMPLES</span></span>

### <span data-ttu-id="a7300-108">Przykład 1: Włączanie zasad usuwania dotyczących przechowywania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="a7300-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="a7300-109">To polecenie umożliwia usuwanie zasad przechowywania dla usługi BLOB i Ustawianie usunięte dni przechowywania obiektów BLOB na wartość 3.</span><span class="sxs-lookup"><span data-stu-id="a7300-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="a7300-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7300-110">PARAMETERS</span></span>

### <span data-ttu-id="a7300-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a7300-111">-Context</span></span>
<span data-ttu-id="a7300-112">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="a7300-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="a7300-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7300-113">-DefaultProfile</span></span>
<span data-ttu-id="a7300-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7300-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7300-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7300-115">-PassThru</span></span>
<span data-ttu-id="a7300-116">Wyświetlanie DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="a7300-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="a7300-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="a7300-117">-RetentionDays</span></span>
<span data-ttu-id="a7300-118">Umożliwia ustawienie liczby dni przechowywania dla DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a7300-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="a7300-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a7300-119">-Confirm</span></span>
<span data-ttu-id="a7300-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7300-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7300-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7300-121">-WhatIf</span></span>
<span data-ttu-id="a7300-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7300-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7300-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a7300-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7300-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7300-124">CommonParameters</span></span>
<span data-ttu-id="a7300-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7300-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7300-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7300-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7300-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7300-127">INPUTS</span></span>

### <span data-ttu-id="a7300-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7300-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a7300-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7300-129">OUTPUTS</span></span>

### <span data-ttu-id="a7300-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7300-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="a7300-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7300-131">NOTES</span></span>

## <span data-ttu-id="a7300-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7300-132">RELATED LINKS</span></span>
