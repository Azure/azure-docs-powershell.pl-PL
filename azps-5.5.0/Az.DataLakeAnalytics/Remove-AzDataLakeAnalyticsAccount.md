---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238219"
---
# <span data-ttu-id="c0003-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0003-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="c0003-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0003-102">SYNOPSIS</span></span>
<span data-ttu-id="c0003-103">Usuwa konto usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0003-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c0003-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0003-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0003-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0003-105">DESCRIPTION</span></span>
<span data-ttu-id="c0003-106">Polecenie **cmdlet Remove-AzDataLakeAnalyticsAccount** trwale usuwa konto usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0003-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c0003-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0003-107">EXAMPLES</span></span>

### <span data-ttu-id="c0003-108">Przykład 1. Usuwanie konta</span><span class="sxs-lookup"><span data-stu-id="c0003-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="c0003-109">To polecenie usuwa określone konto Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0003-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="c0003-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0003-110">PARAMETERS</span></span>

### <span data-ttu-id="c0003-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0003-111">-DefaultProfile</span></span>
<span data-ttu-id="c0003-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c0003-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0003-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c0003-113">-Force</span></span>
<span data-ttu-id="c0003-114">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c0003-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0003-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0003-115">-Name</span></span>
<span data-ttu-id="c0003-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0003-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c0003-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0003-117">-PassThru</span></span>
<span data-ttu-id="c0003-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c0003-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0003-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c0003-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0003-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0003-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0003-121">Określa nazwę grupy zasobów dla konta Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c0003-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c0003-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0003-122">-Confirm</span></span>
<span data-ttu-id="c0003-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0003-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0003-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0003-124">-WhatIf</span></span>
<span data-ttu-id="c0003-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0003-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0003-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0003-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0003-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0003-127">CommonParameters</span></span>
<span data-ttu-id="c0003-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0003-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0003-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0003-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0003-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0003-130">INPUTS</span></span>

### <span data-ttu-id="c0003-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c0003-131">System.String</span></span>

## <span data-ttu-id="c0003-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0003-132">OUTPUTS</span></span>

### <span data-ttu-id="c0003-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0003-133">System.Boolean</span></span>

## <span data-ttu-id="c0003-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0003-134">NOTES</span></span>

## <span data-ttu-id="c0003-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0003-135">RELATED LINKS</span></span>

[<span data-ttu-id="c0003-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0003-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c0003-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0003-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c0003-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0003-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c0003-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c0003-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


