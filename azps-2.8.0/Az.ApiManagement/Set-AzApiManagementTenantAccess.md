---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: dbc1baa96b62e907fd1707bd4ccb4fe007d51ec6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706886"
---
# <span data-ttu-id="42cd5-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="42cd5-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="42cd5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="42cd5-103">Włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="42cd5-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="42cd5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42cd5-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42cd5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="42cd5-106">Polecenie cmdlet **Set-AzApiManagementTenantAccess** włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="42cd5-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="42cd5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42cd5-107">EXAMPLES</span></span>

### <span data-ttu-id="42cd5-108">Przykład 1: Włączanie dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="42cd5-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="42cd5-109">To polecenie umożliwia dostęp dzierżawy w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="42cd5-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="42cd5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42cd5-110">PARAMETERS</span></span>

### <span data-ttu-id="42cd5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="42cd5-111">-Context</span></span>
<span data-ttu-id="42cd5-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="42cd5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="42cd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cd5-113">-DefaultProfile</span></span>
<span data-ttu-id="42cd5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42cd5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42cd5-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="42cd5-115">-Enabled</span></span>
<span data-ttu-id="42cd5-116">Określa, czy to polecenie cmdlet włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="42cd5-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="42cd5-117">Określ wartość $True, aby włączyć lub $False wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="42cd5-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42cd5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42cd5-118">-PassThru</span></span>
<span data-ttu-id="42cd5-119">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementAccessInformation** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42cd5-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="42cd5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cd5-120">CommonParameters</span></span>
<span data-ttu-id="42cd5-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42cd5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cd5-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42cd5-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cd5-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42cd5-123">INPUTS</span></span>

### <span data-ttu-id="42cd5-124">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42cd5-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42cd5-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42cd5-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42cd5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42cd5-126">OUTPUTS</span></span>

### <span data-ttu-id="42cd5-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="42cd5-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="42cd5-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42cd5-128">NOTES</span></span>

## <span data-ttu-id="42cd5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42cd5-129">RELATED LINKS</span></span>

[<span data-ttu-id="42cd5-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="42cd5-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


