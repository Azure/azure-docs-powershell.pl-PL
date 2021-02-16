---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180114"
---
# <span data-ttu-id="16a8e-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="16a8e-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="16a8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="16a8e-103">Usuwanie ustawienia diagnostycznego zasobu.</span><span class="sxs-lookup"><span data-stu-id="16a8e-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="16a8e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16a8e-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16a8e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="16a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="16a8e-106">Polecenie **cmdlet Remove-AzDiagnosticSetting** usuwa ustawienie diagnostyczne dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="16a8e-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="16a8e-107">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed jego utworzeniem, zmodyfikowaniem lub usunięciem.</span><span class="sxs-lookup"><span data-stu-id="16a8e-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="16a8e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16a8e-108">EXAMPLES</span></span>

### <span data-ttu-id="16a8e-109">Przykład 1. Usunięcie domyślnego ustawienia diagnostycznego (usługi) dla zasobu</span><span class="sxs-lookup"><span data-stu-id="16a8e-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="16a8e-110">To polecenie usuwa domyślne ustawienie diagnostyczne (usługa) dla zasobu o nazwie Zasób01.</span><span class="sxs-lookup"><span data-stu-id="16a8e-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="16a8e-111">Przykład 2. Usunięcie domyślnego ustawienia diagnostycznego oznaczonego nazwą zasobu</span><span class="sxs-lookup"><span data-stu-id="16a8e-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="16a8e-112">To polecenie usuwa ustawienie diagnostyczne o nazwie MyDiagSetting dla zasobu o nazwie Zasób01.</span><span class="sxs-lookup"><span data-stu-id="16a8e-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="16a8e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16a8e-113">PARAMETERS</span></span>

### <span data-ttu-id="16a8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a8e-114">-DefaultProfile</span></span>
<span data-ttu-id="16a8e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16a8e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16a8e-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="16a8e-116">-Name</span></span>
<span data-ttu-id="16a8e-117">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="16a8e-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="16a8e-118">Jeśli nie nadano domyślnego ustawienia połączenia "usługa", tak jak w poprzednim interfejsie API, a to polecenie cmdlet wyłączy tylko wszystkie kategorie metryk/dzienników.</span><span class="sxs-lookup"><span data-stu-id="16a8e-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="16a8e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16a8e-119">-ResourceId</span></span>
<span data-ttu-id="16a8e-120">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="16a8e-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="16a8e-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16a8e-121">-Confirm</span></span>
<span data-ttu-id="16a8e-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16a8e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16a8e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16a8e-123">-WhatIf</span></span>
<span data-ttu-id="16a8e-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16a8e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16a8e-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16a8e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16a8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a8e-126">CommonParameters</span></span>
<span data-ttu-id="16a8e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16a8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a8e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16a8e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a8e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16a8e-129">INPUTS</span></span>

### <span data-ttu-id="16a8e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="16a8e-130">System.String</span></span>

## <span data-ttu-id="16a8e-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16a8e-131">OUTPUTS</span></span>

### <span data-ttu-id="16a8e-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="16a8e-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="16a8e-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16a8e-133">NOTES</span></span>

## <span data-ttu-id="16a8e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16a8e-134">RELATED LINKS</span></span>

<span data-ttu-id="16a8e-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="16a8e-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
