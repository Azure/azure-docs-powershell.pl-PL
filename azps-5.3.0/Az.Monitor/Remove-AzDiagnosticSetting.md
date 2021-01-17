---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385679"
---
# <span data-ttu-id="8a4ff-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8a4ff-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="8a4ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4ff-103">Usuwanie ustawienia diagnostycznego dla zasobu a.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="8a4ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a4ff-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a4ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8a4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="8a4ff-106">Polecenie cmdlet **Remove-AzDiagnosticSetting** usuwa ustawienie diagnostyczne konkretnego zasobu.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="8a4ff-107">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8a4ff-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a4ff-108">EXAMPLES</span></span>

### <span data-ttu-id="8a4ff-109">Przykład 1: usuwanie domyślnego ustawienia diagnostycznego (usługi) dla zasobu</span><span class="sxs-lookup"><span data-stu-id="8a4ff-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="8a4ff-110">To polecenie powoduje usunięcie domyślnego ustawienia diagnostycznego (usługi) dla zasobu o nazwie Resource01.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="8a4ff-111">Przykład 2: usuwanie domyślnego ustawienia diagnostycznego określonego dla zasobu</span><span class="sxs-lookup"><span data-stu-id="8a4ff-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="8a4ff-112">To polecenie usuwa ustawienie diagnostyczne o nazwie myDiagSetting dla zasobu o nazwie Resource01.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="8a4ff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a4ff-113">PARAMETERS</span></span>

### <span data-ttu-id="8a4ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4ff-114">-DefaultProfile</span></span>
<span data-ttu-id="8a4ff-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4ff-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a4ff-116">-Name</span></span>
<span data-ttu-id="8a4ff-117">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="8a4ff-118">Jeśli w poprzednim interfejsie API nie ma połączenia z wartością domyślną "usługa", a to polecenie cmdlet spowoduje wyłączenie tylko wszystkich kategorii metryk/dzienników.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="8a4ff-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a4ff-119">-ResourceId</span></span>
<span data-ttu-id="8a4ff-120">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="8a4ff-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a4ff-121">-Confirm</span></span>
<span data-ttu-id="8a4ff-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4ff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4ff-123">-WhatIf</span></span>
<span data-ttu-id="8a4ff-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a4ff-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4ff-126">CommonParameters</span></span>
<span data-ttu-id="8a4ff-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a4ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4ff-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a4ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4ff-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a4ff-129">INPUTS</span></span>

### <span data-ttu-id="8a4ff-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8a4ff-130">System.String</span></span>

## <span data-ttu-id="8a4ff-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a4ff-131">OUTPUTS</span></span>

### <span data-ttu-id="8a4ff-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8a4ff-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8a4ff-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a4ff-133">NOTES</span></span>

## <span data-ttu-id="8a4ff-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a4ff-134">RELATED LINKS</span></span>

<span data-ttu-id="8a4ff-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="8a4ff-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
