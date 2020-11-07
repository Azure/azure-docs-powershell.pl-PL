---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 5e62bc19ec400f3dbfff3c089880cd14ce95609e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705872"
---
# <span data-ttu-id="a4712-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a4712-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a4712-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4712-102">SYNOPSIS</span></span>
<span data-ttu-id="a4712-103">Usuwa konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4712-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a4712-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4712-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4712-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4712-105">DESCRIPTION</span></span>
<span data-ttu-id="a4712-106">Polecenie cmdlet **Remove-AzDataLakeAnalyticsAccount** powoduje trwałe usunięcie konta usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4712-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a4712-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4712-107">EXAMPLES</span></span>

### <span data-ttu-id="a4712-108">Przykład 1. Usuń konto</span><span class="sxs-lookup"><span data-stu-id="a4712-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="a4712-109">To polecenie umożliwia usunięcie określonego konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4712-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="a4712-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4712-110">PARAMETERS</span></span>

### <span data-ttu-id="a4712-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4712-111">-DefaultProfile</span></span>
<span data-ttu-id="a4712-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a4712-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4712-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a4712-113">-Force</span></span>
<span data-ttu-id="a4712-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a4712-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4712-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4712-115">-Name</span></span>
<span data-ttu-id="a4712-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4712-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a4712-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4712-117">-PassThru</span></span>
<span data-ttu-id="a4712-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a4712-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a4712-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a4712-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4712-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4712-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4712-121">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4712-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a4712-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4712-122">-Confirm</span></span>
<span data-ttu-id="a4712-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4712-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4712-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4712-124">-WhatIf</span></span>
<span data-ttu-id="a4712-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4712-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4712-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4712-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4712-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4712-127">CommonParameters</span></span>
<span data-ttu-id="a4712-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4712-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4712-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4712-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4712-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4712-130">INPUTS</span></span>

### <span data-ttu-id="a4712-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a4712-131">System.String</span></span>

## <span data-ttu-id="a4712-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4712-132">OUTPUTS</span></span>

### <span data-ttu-id="a4712-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4712-133">System.Boolean</span></span>

## <span data-ttu-id="a4712-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4712-134">NOTES</span></span>

## <span data-ttu-id="a4712-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4712-135">RELATED LINKS</span></span>

[<span data-ttu-id="a4712-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a4712-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a4712-137">Nowe — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a4712-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a4712-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a4712-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a4712-139">Test — AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a4712-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)

