---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 135dced6c66f1212f172a2c435a7468b16e71708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524689"
---
# <span data-ttu-id="55940-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="55940-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="55940-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55940-102">SYNOPSIS</span></span>
<span data-ttu-id="55940-103">Usuwa rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="55940-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55940-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55940-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55940-105">Opis</span><span class="sxs-lookup"><span data-stu-id="55940-105">DESCRIPTION</span></span>
<span data-ttu-id="55940-106">Polecenie cmdlet **Remove-AzureRmApiManagementLogger** usuwa **Rejestrator** zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="55940-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="55940-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55940-107">EXAMPLES</span></span>

### <span data-ttu-id="55940-108">Przykład 1: usuwanie rejestratora</span><span class="sxs-lookup"><span data-stu-id="55940-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="55940-109">To polecenie usuwa rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="55940-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="55940-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55940-110">PARAMETERS</span></span>

### <span data-ttu-id="55940-111">-Context</span><span class="sxs-lookup"><span data-stu-id="55940-111">-Context</span></span>
<span data-ttu-id="55940-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="55940-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55940-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55940-113">-DefaultProfile</span></span>
<span data-ttu-id="55940-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55940-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55940-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="55940-115">-LoggerId</span></span>
<span data-ttu-id="55940-116">Określa identyfikator rejestratora, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="55940-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="55940-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55940-117">-PassThru</span></span>
<span data-ttu-id="55940-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli operacja się powiedzie lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="55940-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="55940-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55940-119">-Confirm</span></span>
<span data-ttu-id="55940-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55940-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55940-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55940-121">-WhatIf</span></span>
<span data-ttu-id="55940-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55940-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55940-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55940-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55940-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55940-124">CommonParameters</span></span>
<span data-ttu-id="55940-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55940-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55940-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55940-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55940-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55940-127">INPUTS</span></span>

### <span data-ttu-id="55940-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="55940-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="55940-129">System. String</span><span class="sxs-lookup"><span data-stu-id="55940-129">System.String</span></span>

### <span data-ttu-id="55940-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55940-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55940-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55940-131">OUTPUTS</span></span>

### <span data-ttu-id="55940-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55940-132">System.Boolean</span></span>

## <span data-ttu-id="55940-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55940-133">NOTES</span></span>

## <span data-ttu-id="55940-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55940-134">RELATED LINKS</span></span>

[<span data-ttu-id="55940-135">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="55940-135">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="55940-136">Nowe — AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="55940-136">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="55940-137">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="55940-137">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


