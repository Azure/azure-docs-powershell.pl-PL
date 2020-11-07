---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869344"
---
# <span data-ttu-id="d2f72-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2f72-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="d2f72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2f72-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f72-103">Umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d2f72-103">Configures an API management group.</span></span>

## <span data-ttu-id="d2f72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2f72-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2f72-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2f72-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f72-106">Polecenie cmdlet **Set-AzApiManagementGroup** umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d2f72-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="d2f72-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2f72-107">EXAMPLES</span></span>

### <span data-ttu-id="d2f72-108">Przykład 1: Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="d2f72-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="d2f72-109">To polecenie umożliwia skonfigurowanie grupy zarządzania o nazwie Group0001.</span><span class="sxs-lookup"><span data-stu-id="d2f72-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="d2f72-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2f72-110">PARAMETERS</span></span>

### <span data-ttu-id="d2f72-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d2f72-111">-Context</span></span>
<span data-ttu-id="d2f72-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d2f72-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d2f72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f72-113">-DefaultProfile</span></span>
<span data-ttu-id="d2f72-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f72-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2f72-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="d2f72-115">-Description</span></span>
<span data-ttu-id="d2f72-116">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d2f72-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="d2f72-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d2f72-117">-GroupId</span></span>
<span data-ttu-id="d2f72-118">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d2f72-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="d2f72-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2f72-119">-Name</span></span>
<span data-ttu-id="d2f72-120">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d2f72-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="d2f72-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2f72-121">-PassThru</span></span>
<span data-ttu-id="d2f72-122">passthru</span><span class="sxs-lookup"><span data-stu-id="d2f72-122">passthru</span></span>

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

### <span data-ttu-id="d2f72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f72-123">CommonParameters</span></span>
<span data-ttu-id="d2f72-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f72-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f72-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2f72-126">INPUTS</span></span>

### <span data-ttu-id="d2f72-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2f72-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d2f72-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d2f72-128">System.String</span></span>

### <span data-ttu-id="d2f72-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2f72-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2f72-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2f72-130">OUTPUTS</span></span>

### <span data-ttu-id="d2f72-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2f72-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="d2f72-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2f72-132">NOTES</span></span>

## <span data-ttu-id="d2f72-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2f72-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2f72-134">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2f72-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="d2f72-135">Nowe — AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2f72-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="d2f72-136">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2f72-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


