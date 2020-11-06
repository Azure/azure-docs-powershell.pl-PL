---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552444"
---
# <span data-ttu-id="d10ba-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d10ba-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="d10ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d10ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d10ba-103">Umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d10ba-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d10ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d10ba-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d10ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d10ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d10ba-106">Polecenie cmdlet **Set-AzureRmApiManagementGroup** umożliwia skonfigurowanie grupy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d10ba-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="d10ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d10ba-107">EXAMPLES</span></span>

### <span data-ttu-id="d10ba-108">Przykład 1: Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="d10ba-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="d10ba-109">To polecenie umożliwia skonfigurowanie grupy zarządzania o nazwie Group0001.</span><span class="sxs-lookup"><span data-stu-id="d10ba-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="d10ba-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d10ba-110">PARAMETERS</span></span>

### <span data-ttu-id="d10ba-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d10ba-111">-Context</span></span>
<span data-ttu-id="d10ba-112">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d10ba-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d10ba-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="d10ba-113">-Description</span></span>
<span data-ttu-id="d10ba-114">Określa opis grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d10ba-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="d10ba-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d10ba-115">-GroupId</span></span>
<span data-ttu-id="d10ba-116">Określa identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d10ba-116">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="d10ba-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d10ba-117">-Name</span></span>
<span data-ttu-id="d10ba-118">Określa nazwę grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d10ba-118">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="d10ba-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d10ba-119">-PassThru</span></span>
<span data-ttu-id="d10ba-120">passthru</span><span class="sxs-lookup"><span data-stu-id="d10ba-120">passthru</span></span>

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

### <span data-ttu-id="d10ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10ba-121">-DefaultProfile</span></span>
<span data-ttu-id="d10ba-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d10ba-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d10ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10ba-123">CommonParameters</span></span>
<span data-ttu-id="d10ba-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d10ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10ba-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10ba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10ba-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d10ba-126">INPUTS</span></span>

## <span data-ttu-id="d10ba-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d10ba-127">OUTPUTS</span></span>

### <span data-ttu-id="d10ba-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d10ba-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="d10ba-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d10ba-129">NOTES</span></span>

## <span data-ttu-id="d10ba-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d10ba-130">RELATED LINKS</span></span>

[<span data-ttu-id="d10ba-131">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d10ba-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d10ba-132">Nowe — AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d10ba-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d10ba-133">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d10ba-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


