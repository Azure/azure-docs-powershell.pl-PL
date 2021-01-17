---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323456"
---
# <span data-ttu-id="2a58c-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="2a58c-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="2a58c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a58c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a58c-103">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2a58c-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="2a58c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a58c-104">SYNTAX</span></span>

### <span data-ttu-id="2a58c-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a58c-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a58c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a58c-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a58c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a58c-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a58c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2a58c-108">DESCRIPTION</span></span>
<span data-ttu-id="2a58c-109">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2a58c-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="2a58c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a58c-110">EXAMPLES</span></span>

### <span data-ttu-id="2a58c-111">Uzyskiwanie klawiszy dostępu dla konkretnej usługi sygnalizacji</span><span class="sxs-lookup"><span data-stu-id="2a58c-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="2a58c-112">Uzyskiwanie kluczy dostępu z obiektu usługi sygnalizacji w potoku</span><span class="sxs-lookup"><span data-stu-id="2a58c-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="2a58c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a58c-113">PARAMETERS</span></span>

### <span data-ttu-id="2a58c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a58c-114">-DefaultProfile</span></span>
<span data-ttu-id="2a58c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a58c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a58c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2a58c-116">-InputObject</span></span>
<span data-ttu-id="2a58c-117">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2a58c-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="2a58c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a58c-118">-Name</span></span>
<span data-ttu-id="2a58c-119">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2a58c-119">SignalR service name.</span></span>

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

### <span data-ttu-id="2a58c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a58c-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a58c-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a58c-121">Resource group name.</span></span>

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

### <span data-ttu-id="2a58c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a58c-122">-ResourceId</span></span>
<span data-ttu-id="2a58c-123">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2a58c-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="2a58c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a58c-124">CommonParameters</span></span>
<span data-ttu-id="2a58c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a58c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a58c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a58c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a58c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a58c-127">INPUTS</span></span>

### <span data-ttu-id="2a58c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2a58c-128">System.String</span></span>
### <span data-ttu-id="2a58c-129">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="2a58c-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="2a58c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a58c-130">OUTPUTS</span></span>

### <span data-ttu-id="2a58c-131">Microsoft. Azure. Commands. Signals. modele. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="2a58c-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="2a58c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a58c-132">NOTES</span></span>

## <span data-ttu-id="2a58c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a58c-133">RELATED LINKS</span></span>
