---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717184"
---
# <span data-ttu-id="485ee-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="485ee-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="485ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="485ee-102">SYNOPSIS</span></span>
<span data-ttu-id="485ee-103">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="485ee-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="485ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="485ee-104">SYNTAX</span></span>

### <span data-ttu-id="485ee-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="485ee-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="485ee-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="485ee-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="485ee-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="485ee-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="485ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="485ee-108">DESCRIPTION</span></span>
<span data-ttu-id="485ee-109">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="485ee-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="485ee-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="485ee-110">EXAMPLES</span></span>

### <span data-ttu-id="485ee-111">Uzyskiwanie klawiszy dostępu dla konkretnej usługi sygnalizacji</span><span class="sxs-lookup"><span data-stu-id="485ee-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="485ee-112">Uzyskiwanie kluczy dostępu z obiektu usługi sygnalizacji w potoku</span><span class="sxs-lookup"><span data-stu-id="485ee-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="485ee-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="485ee-113">PARAMETERS</span></span>

### <span data-ttu-id="485ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485ee-114">-DefaultProfile</span></span>
<span data-ttu-id="485ee-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="485ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="485ee-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="485ee-116">-InputObject</span></span>
<span data-ttu-id="485ee-117">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="485ee-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="485ee-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="485ee-118">-Name</span></span>
<span data-ttu-id="485ee-119">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="485ee-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="485ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="485ee-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="485ee-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="485ee-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="485ee-122">-ResourceId</span></span>
<span data-ttu-id="485ee-123">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="485ee-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="485ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485ee-124">CommonParameters</span></span>
<span data-ttu-id="485ee-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485ee-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="485ee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485ee-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="485ee-127">INPUTS</span></span>

### <span data-ttu-id="485ee-128">System. String</span><span class="sxs-lookup"><span data-stu-id="485ee-128">System.String</span></span>
<span data-ttu-id="485ee-129">Parametry: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="485ee-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="485ee-130">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="485ee-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="485ee-131">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="485ee-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="485ee-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="485ee-132">OUTPUTS</span></span>

### <span data-ttu-id="485ee-133">Microsoft. Azure. Commands. Signals. modele. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="485ee-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="485ee-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="485ee-134">NOTES</span></span>

## <span data-ttu-id="485ee-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="485ee-135">RELATED LINKS</span></span>
