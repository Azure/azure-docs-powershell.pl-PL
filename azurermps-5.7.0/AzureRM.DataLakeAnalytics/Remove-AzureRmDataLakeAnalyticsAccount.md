---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: f978925766fb664f5ddeaf3b6dffa94e55244f43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716845"
---
# <span data-ttu-id="1ffa7-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1ffa7-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="1ffa7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ffa7-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffa7-103">Usuwa konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ffa7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ffa7-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ffa7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ffa7-105">DESCRIPTION</span></span>
<span data-ttu-id="1ffa7-106">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsAccount** powoduje trwałe usunięcie konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1ffa7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ffa7-107">EXAMPLES</span></span>

### <span data-ttu-id="1ffa7-108">Przykład 1. Usuń konto</span><span class="sxs-lookup"><span data-stu-id="1ffa7-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="1ffa7-109">To polecenie umożliwia usunięcie określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="1ffa7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ffa7-110">PARAMETERS</span></span>

### <span data-ttu-id="1ffa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffa7-111">-DefaultProfile</span></span>
<span data-ttu-id="1ffa7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1ffa7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffa7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1ffa7-113">-Force</span></span>
<span data-ttu-id="1ffa7-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffa7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ffa7-115">-Name</span></span>
<span data-ttu-id="1ffa7-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ffa7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ffa7-117">-PassThru</span></span>
<span data-ttu-id="1ffa7-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1ffa7-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffa7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffa7-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ffa7-121">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ffa7-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ffa7-122">-Confirm</span></span>
<span data-ttu-id="1ffa7-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffa7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ffa7-124">-WhatIf</span></span>
<span data-ttu-id="1ffa7-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ffa7-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffa7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffa7-127">CommonParameters</span></span>
<span data-ttu-id="1ffa7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffa7-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ffa7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffa7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ffa7-130">INPUTS</span></span>

### <span data-ttu-id="1ffa7-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1ffa7-131">None</span></span>
<span data-ttu-id="1ffa7-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ffa7-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ffa7-133">OUTPUTS</span></span>

### <span data-ttu-id="1ffa7-134">logiczną</span><span class="sxs-lookup"><span data-stu-id="1ffa7-134">bool</span></span>
<span data-ttu-id="1ffa7-135">Jeśli PassThru jest określony, zwraca wartość Prawda po wykonaniu operacji.</span><span class="sxs-lookup"><span data-stu-id="1ffa7-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="1ffa7-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ffa7-136">NOTES</span></span>

## <span data-ttu-id="1ffa7-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ffa7-137">RELATED LINKS</span></span>

[<span data-ttu-id="1ffa7-138">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1ffa7-138">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1ffa7-139">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1ffa7-139">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1ffa7-140">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1ffa7-140">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="1ffa7-141">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="1ffa7-141">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


