---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: 85d391e3f50bb06ddbc5ec8937b643d9dcbce492
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959514"
---
# <span data-ttu-id="bb1ab-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="bb1ab-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="bb1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1ab-103">Usuwanie ustawienia diagnostycznego zasobu.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="bb1ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb1ab-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb1ab-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb1ab-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1ab-106">Polecenie **cmdlet Remove-AzDiagnosticSetting** usuwa ustawienie diagnostyczne dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="bb1ab-107">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="bb1ab-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb1ab-108">EXAMPLES</span></span>

### <span data-ttu-id="bb1ab-109">Przykład 1. Usunięcie domyślnego ustawienia diagnostycznego (usługi) dla zasobu</span><span class="sxs-lookup"><span data-stu-id="bb1ab-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="bb1ab-110">To polecenie usuwa domyślne ustawienie diagnostyczne (usługi) dla zasobu o nazwie Zasób01.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="bb1ab-111">Przykład 2. Usunięcie domyślnego ustawienia diagnostycznego oznaczonego nazwą zasobu</span><span class="sxs-lookup"><span data-stu-id="bb1ab-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="bb1ab-112">To polecenie usuwa ustawienie diagnostyczne o nazwie MyDiagSetting dla zasobu o nazwie Zasób01.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="bb1ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb1ab-113">PARAMETERS</span></span>

### <span data-ttu-id="bb1ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1ab-114">-DefaultProfile</span></span>
<span data-ttu-id="bb1ab-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb1ab-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb1ab-116">-Name</span></span>
<span data-ttu-id="bb1ab-117">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="bb1ab-118">Jeśli nie nadano domyślnego ustawienia "usługa", tak jak w poprzednim interfejsie API, a to polecenie cmdlet wyłączy tylko wszystkie kategorie metryk/dzienników.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1ab-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb1ab-119">-ResourceId</span></span>
<span data-ttu-id="bb1ab-120">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-120">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1ab-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb1ab-121">-Confirm</span></span>
<span data-ttu-id="bb1ab-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb1ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb1ab-123">-WhatIf</span></span>
<span data-ttu-id="bb1ab-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb1ab-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb1ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1ab-126">CommonParameters</span></span>
<span data-ttu-id="bb1ab-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1ab-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb1ab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1ab-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb1ab-129">INPUTS</span></span>

### <span data-ttu-id="bb1ab-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bb1ab-130">System.String</span></span>

## <span data-ttu-id="bb1ab-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb1ab-131">OUTPUTS</span></span>

### <span data-ttu-id="bb1ab-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bb1ab-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="bb1ab-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb1ab-133">NOTES</span></span>

## <span data-ttu-id="bb1ab-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb1ab-134">RELATED LINKS</span></span>

<span data-ttu-id="bb1ab-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="bb1ab-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
