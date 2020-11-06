---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c75aceee59e5696d928f19fa6d5ae317828fa82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525746"
---
# <span data-ttu-id="cd1f7-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="cd1f7-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="cd1f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1f7-103">Włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd1f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd1f7-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd1f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd1f7-105">DESCRIPTION</span></span>
<span data-ttu-id="cd1f7-106">Polecenie cmdlet **Set-AzureRmApiManagementTenantAccess** włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="cd1f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd1f7-107">EXAMPLES</span></span>

### <span data-ttu-id="cd1f7-108">Przykład 1: Włączanie dostępu do dzierżawy</span><span class="sxs-lookup"><span data-stu-id="cd1f7-108">Example 1: Enable tenant access</span></span>
```
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $ApimContext -Enabled $True
```

<span data-ttu-id="cd1f7-109">To polecenie umożliwia dostęp dzierżawy w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="cd1f7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd1f7-110">PARAMETERS</span></span>

### <span data-ttu-id="cd1f7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cd1f7-111">-Context</span></span>
<span data-ttu-id="cd1f7-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cd1f7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cd1f7-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="cd1f7-113">-Enabled</span></span>
<span data-ttu-id="cd1f7-114">Określa, czy to polecenie cmdlet włącza lub wyłącza dostęp dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-114">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="cd1f7-115">Określ wartość $True, aby włączyć lub $False wyłączyć.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-115">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="cd1f7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd1f7-116">-PassThru</span></span>
<span data-ttu-id="cd1f7-117">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementAccessInformation** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-117">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cd1f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1f7-118">-DefaultProfile</span></span>
<span data-ttu-id="cd1f7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd1f7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1f7-120">CommonParameters</span></span>
<span data-ttu-id="cd1f7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1f7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1f7-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd1f7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1f7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd1f7-123">INPUTS</span></span>

## <span data-ttu-id="cd1f7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd1f7-124">OUTPUTS</span></span>

### <span data-ttu-id="cd1f7-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="cd1f7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="cd1f7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd1f7-126">NOTES</span></span>

## <span data-ttu-id="cd1f7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd1f7-127">RELATED LINKS</span></span>

[<span data-ttu-id="cd1f7-128">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="cd1f7-128">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


