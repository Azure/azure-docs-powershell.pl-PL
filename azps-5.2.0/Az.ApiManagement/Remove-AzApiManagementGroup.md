---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361384"
---
# <span data-ttu-id="db915-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="db915-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="db915-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db915-102">SYNOPSIS</span></span>
<span data-ttu-id="db915-103">Usuwa istniejącą grupę zarządzania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="db915-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="db915-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db915-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db915-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db915-105">DESCRIPTION</span></span>
<span data-ttu-id="db915-106">Polecenie cmdlet **Remove-AzApiManagementGroup** Usuwa istniejącą grupę zarządzania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="db915-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="db915-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db915-107">EXAMPLES</span></span>

### <span data-ttu-id="db915-108">Przykład 1. Usuń istniejącą grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="db915-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="db915-109">To polecenie usuwa istniejącą grupę zarządzania o nazwie Group0001 i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="db915-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="db915-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db915-110">PARAMETERS</span></span>

### <span data-ttu-id="db915-111">-Context</span><span class="sxs-lookup"><span data-stu-id="db915-111">-Context</span></span>
<span data-ttu-id="db915-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="db915-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db915-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db915-113">-DefaultProfile</span></span>
<span data-ttu-id="db915-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db915-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db915-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="db915-115">-GroupId</span></span>
<span data-ttu-id="db915-116">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="db915-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="db915-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db915-117">-PassThru</span></span>
<span data-ttu-id="db915-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli ta operacja się powiedzie lub wartość $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="db915-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db915-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db915-119">-Confirm</span></span>
<span data-ttu-id="db915-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db915-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db915-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db915-121">-WhatIf</span></span>
<span data-ttu-id="db915-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db915-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db915-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="db915-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db915-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db915-124">CommonParameters</span></span>
<span data-ttu-id="db915-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db915-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db915-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db915-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db915-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db915-127">INPUTS</span></span>

### <span data-ttu-id="db915-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db915-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db915-129">System. String</span><span class="sxs-lookup"><span data-stu-id="db915-129">System.String</span></span>

### <span data-ttu-id="db915-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db915-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db915-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db915-131">OUTPUTS</span></span>

### <span data-ttu-id="db915-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db915-132">System.Boolean</span></span>

## <span data-ttu-id="db915-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db915-133">NOTES</span></span>

## <span data-ttu-id="db915-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db915-134">RELATED LINKS</span></span>

[<span data-ttu-id="db915-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="db915-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="db915-136">Nowe — AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="db915-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="db915-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="db915-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


