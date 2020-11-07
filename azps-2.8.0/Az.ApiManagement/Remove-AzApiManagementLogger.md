---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: ff8a4427a909af35d8e8a910210e559212a6b7c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706948"
---
# <span data-ttu-id="ab2f7-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ab2f7-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="ab2f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2f7-103">Usuwa rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="ab2f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab2f7-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab2f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2f7-106">Polecenie cmdlet **Remove-AzApiManagementLogger** usuwa **Rejestrator** zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="ab2f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab2f7-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2f7-108">Przykład 1: usuwanie rejestratora</span><span class="sxs-lookup"><span data-stu-id="ab2f7-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="ab2f7-109">To polecenie usuwa rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="ab2f7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab2f7-110">PARAMETERS</span></span>

### <span data-ttu-id="ab2f7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ab2f7-111">-Context</span></span>
<span data-ttu-id="ab2f7-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ab2f7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ab2f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2f7-113">-DefaultProfile</span></span>
<span data-ttu-id="ab2f7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab2f7-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="ab2f7-115">-LoggerId</span></span>
<span data-ttu-id="ab2f7-116">Określa identyfikator rejestratora, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="ab2f7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab2f7-117">-PassThru</span></span>
<span data-ttu-id="ab2f7-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="ab2f7-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab2f7-119">-Confirm</span></span>
<span data-ttu-id="ab2f7-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab2f7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2f7-121">-WhatIf</span></span>
<span data-ttu-id="ab2f7-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab2f7-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab2f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2f7-124">CommonParameters</span></span>
<span data-ttu-id="ab2f7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2f7-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab2f7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2f7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab2f7-127">INPUTS</span></span>

### <span data-ttu-id="ab2f7-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab2f7-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab2f7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ab2f7-129">System.String</span></span>

### <span data-ttu-id="ab2f7-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab2f7-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab2f7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab2f7-131">OUTPUTS</span></span>

### <span data-ttu-id="ab2f7-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab2f7-132">System.Boolean</span></span>

## <span data-ttu-id="ab2f7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab2f7-133">NOTES</span></span>

## <span data-ttu-id="ab2f7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab2f7-134">RELATED LINKS</span></span>

[<span data-ttu-id="ab2f7-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ab2f7-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="ab2f7-136">Nowe — AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ab2f7-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="ab2f7-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ab2f7-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


