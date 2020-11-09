---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317586"
---
# <span data-ttu-id="2e91a-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="2e91a-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="2e91a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e91a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e91a-103">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2e91a-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="2e91a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e91a-104">SYNTAX</span></span>

### <span data-ttu-id="2e91a-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e91a-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e91a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e91a-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e91a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e91a-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e91a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e91a-108">DESCRIPTION</span></span>
<span data-ttu-id="2e91a-109">Uzyskaj klucze dostępu do usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2e91a-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="2e91a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e91a-110">EXAMPLES</span></span>

### <span data-ttu-id="2e91a-111">Uzyskiwanie klawiszy dostępu dla konkretnej usługi sygnalizacji</span><span class="sxs-lookup"><span data-stu-id="2e91a-111">Get access keys of a specific SignalR service</span></span>
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

### <span data-ttu-id="2e91a-112">Uzyskiwanie kluczy dostępu z obiektu usługi sygnalizacji w potoku</span><span class="sxs-lookup"><span data-stu-id="2e91a-112">Get access keys from a SignalR service object in pipe</span></span>

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

## <span data-ttu-id="2e91a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e91a-113">PARAMETERS</span></span>

### <span data-ttu-id="2e91a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e91a-114">-DefaultProfile</span></span>
<span data-ttu-id="2e91a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e91a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e91a-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e91a-116">-InputObject</span></span>
<span data-ttu-id="2e91a-117">Obiekt zasobu sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2e91a-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="2e91a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e91a-118">-Name</span></span>
<span data-ttu-id="2e91a-119">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2e91a-119">SignalR service name.</span></span>

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

### <span data-ttu-id="2e91a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e91a-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e91a-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e91a-121">Resource group name.</span></span>

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

### <span data-ttu-id="2e91a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e91a-122">-ResourceId</span></span>
<span data-ttu-id="2e91a-123">Identyfikator zasobu usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="2e91a-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="2e91a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e91a-124">CommonParameters</span></span>
<span data-ttu-id="2e91a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e91a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e91a-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e91a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e91a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e91a-127">INPUTS</span></span>

### <span data-ttu-id="2e91a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2e91a-128">System.String</span></span>
### <span data-ttu-id="2e91a-129">Microsoft. Azure. Commands. Signals. modele. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="2e91a-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="2e91a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e91a-130">OUTPUTS</span></span>

### <span data-ttu-id="2e91a-131">Microsoft. Azure. Commands. Signals. modele. PSSignalRKeys</span><span class="sxs-lookup"><span data-stu-id="2e91a-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="2e91a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e91a-132">NOTES</span></span>

## <span data-ttu-id="2e91a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e91a-133">RELATED LINKS</span></span>
