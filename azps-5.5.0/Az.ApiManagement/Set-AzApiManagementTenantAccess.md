---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244331"
---
# <span data-ttu-id="aca9c-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="aca9c-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="aca9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca9c-102">SYNOPSIS</span></span>
<span data-ttu-id="aca9c-103">Włączenie lub wyłączenie dostępu do dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="aca9c-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="aca9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aca9c-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aca9c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aca9c-105">DESCRIPTION</span></span>
<span data-ttu-id="aca9c-106">Polecenie **cmdlet Set-AzApiManagementTenantAccess** włącza lub wyłącza dostęp do dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="aca9c-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="aca9c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aca9c-107">EXAMPLES</span></span>

### <span data-ttu-id="aca9c-108">Przykład 1. Włączanie dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="aca9c-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="aca9c-109">To polecenie umożliwia dostęp do dzierżawy w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="aca9c-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="aca9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aca9c-110">PARAMETERS</span></span>

### <span data-ttu-id="aca9c-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="aca9c-111">-Context</span></span>
<span data-ttu-id="aca9c-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="aca9c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aca9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca9c-113">-DefaultProfile</span></span>
<span data-ttu-id="aca9c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aca9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aca9c-115">— włączone</span><span class="sxs-lookup"><span data-stu-id="aca9c-115">-Enabled</span></span>
<span data-ttu-id="aca9c-116">Określa, czy to polecenie cmdlet włącza lub wyłącza dostęp do dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="aca9c-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="aca9c-117">Określ wartość określającą, $True włączyć lub $False wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="aca9c-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="aca9c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aca9c-118">-PassThru</span></span>
<span data-ttu-id="aca9c-119">Wskazuje, że to polecenie cmdlet zwraca polecenie **PsApiManagementAccessInformation,** które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="aca9c-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aca9c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca9c-120">CommonParameters</span></span>
<span data-ttu-id="aca9c-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aca9c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca9c-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aca9c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca9c-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aca9c-123">INPUTS</span></span>

### <span data-ttu-id="aca9c-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aca9c-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aca9c-125">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="aca9c-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aca9c-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aca9c-126">OUTPUTS</span></span>

### <span data-ttu-id="aca9c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="aca9c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="aca9c-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aca9c-128">NOTES</span></span>

## <span data-ttu-id="aca9c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aca9c-129">RELATED LINKS</span></span>

[<span data-ttu-id="aca9c-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="aca9c-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


