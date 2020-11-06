---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 058a82398be387913a0dd3eaf58c80ac12b692dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526402"
---
# <span data-ttu-id="fa58b-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fa58b-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="fa58b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa58b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa58b-103">Umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="fa58b-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa58b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa58b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa58b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa58b-105">DESCRIPTION</span></span>
<span data-ttu-id="fa58b-106">Polecenie cmdlet **Set-AzureRmApiManagementGroup** umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="fa58b-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="fa58b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa58b-107">EXAMPLES</span></span>

### <span data-ttu-id="fa58b-108">Przykład 1: Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="fa58b-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="fa58b-109">To polecenie umożliwia skonfigurowanie grupy zarządzania o nazwie Group0001.</span><span class="sxs-lookup"><span data-stu-id="fa58b-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="fa58b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa58b-110">PARAMETERS</span></span>

### <span data-ttu-id="fa58b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fa58b-111">-Context</span></span>
<span data-ttu-id="fa58b-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fa58b-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fa58b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa58b-113">-DefaultProfile</span></span>
<span data-ttu-id="fa58b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa58b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa58b-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="fa58b-115">-Description</span></span>
<span data-ttu-id="fa58b-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="fa58b-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="fa58b-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fa58b-117">-GroupId</span></span>
<span data-ttu-id="fa58b-118">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="fa58b-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="fa58b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fa58b-119">-Name</span></span>
<span data-ttu-id="fa58b-120">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="fa58b-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="fa58b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa58b-121">-PassThru</span></span>
<span data-ttu-id="fa58b-122">passthru</span><span class="sxs-lookup"><span data-stu-id="fa58b-122">passthru</span></span>

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

### <span data-ttu-id="fa58b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa58b-123">CommonParameters</span></span>
<span data-ttu-id="fa58b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa58b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa58b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa58b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa58b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa58b-126">INPUTS</span></span>

### <span data-ttu-id="fa58b-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fa58b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fa58b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fa58b-128">System.String</span></span>

### <span data-ttu-id="fa58b-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa58b-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa58b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa58b-130">OUTPUTS</span></span>

### <span data-ttu-id="fa58b-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fa58b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="fa58b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa58b-132">NOTES</span></span>

## <span data-ttu-id="fa58b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa58b-133">RELATED LINKS</span></span>

[<span data-ttu-id="fa58b-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fa58b-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="fa58b-135">Nowe — AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fa58b-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="fa58b-136">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fa58b-136">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


