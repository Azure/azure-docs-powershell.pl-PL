---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a04295bca6c664e583ae9653b1f3ed7d52aebf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718335"
---
# <span data-ttu-id="5d29e-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5d29e-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="5d29e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d29e-102">SYNOPSIS</span></span>
<span data-ttu-id="5d29e-103">Usuwa konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d29e-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d29e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d29e-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d29e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5d29e-105">DESCRIPTION</span></span>
<span data-ttu-id="5d29e-106">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsAccount** powoduje trwałe usunięcie konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d29e-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5d29e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d29e-107">EXAMPLES</span></span>

### <span data-ttu-id="5d29e-108">Przykład 1. Usuń konto</span><span class="sxs-lookup"><span data-stu-id="5d29e-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="5d29e-109">To polecenie umożliwia usunięcie określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d29e-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="5d29e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d29e-110">PARAMETERS</span></span>

### <span data-ttu-id="5d29e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d29e-111">-DefaultProfile</span></span>
<span data-ttu-id="5d29e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d29e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d29e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5d29e-113">-Force</span></span>
<span data-ttu-id="5d29e-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5d29e-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d29e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d29e-115">-Name</span></span>
<span data-ttu-id="5d29e-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d29e-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d29e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d29e-117">-PassThru</span></span>
<span data-ttu-id="5d29e-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5d29e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5d29e-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5d29e-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d29e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d29e-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d29e-121">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d29e-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d29e-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d29e-122">-Confirm</span></span>
<span data-ttu-id="5d29e-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d29e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d29e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d29e-124">-WhatIf</span></span>
<span data-ttu-id="5d29e-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d29e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d29e-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d29e-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d29e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d29e-127">CommonParameters</span></span>
<span data-ttu-id="5d29e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d29e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d29e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d29e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d29e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d29e-130">INPUTS</span></span>

### <span data-ttu-id="5d29e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5d29e-131">System.String</span></span>

## <span data-ttu-id="5d29e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d29e-132">OUTPUTS</span></span>

### <span data-ttu-id="5d29e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d29e-133">System.Boolean</span></span>

## <span data-ttu-id="5d29e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d29e-134">NOTES</span></span>

## <span data-ttu-id="5d29e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d29e-135">RELATED LINKS</span></span>

[<span data-ttu-id="5d29e-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5d29e-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5d29e-137">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5d29e-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5d29e-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5d29e-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="5d29e-139">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="5d29e-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


