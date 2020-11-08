---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055288"
---
# <span data-ttu-id="3e44c-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="3e44c-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="3e44c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e44c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e44c-103">Pobiera wynik operacji usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3e44c-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="3e44c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e44c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3e44c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e44c-105">DESCRIPTION</span></span>
<span data-ttu-id="3e44c-106">Polecenie cmdlet **Get-AzureRemoteAppOperationResult** pobiera wyniki długotrwałej operacji na platformie Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3e44c-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="3e44c-107">Usługa Azure RemoteApp używa długotrwałych operacji dla wielu akcji wymagających przetworzenia przez usługę i nie może zwrócić jej natychmiast.</span><span class="sxs-lookup"><span data-stu-id="3e44c-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="3e44c-108">Przykłady poleceń cmdlet, które zwracają identyfikatory śledzenia, obejmują **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** i inne.</span><span class="sxs-lookup"><span data-stu-id="3e44c-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="3e44c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e44c-109">EXAMPLES</span></span>

### <span data-ttu-id="3e44c-110">Przykład 1. Aby uzyskać wynik operacji, użyj identyfikatora śledzenia</span><span class="sxs-lookup"><span data-stu-id="3e44c-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="3e44c-111">To polecenie zapisuje identyfikator śledzenia zwrócony przez operację usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3e44c-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="3e44c-112">Identyfikator śledzenia jest przekazywany do polecenia **Get-AzureRemoteAppOperationResult** w poniższym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="3e44c-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="3e44c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e44c-113">PARAMETERS</span></span>

### <span data-ttu-id="3e44c-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="3e44c-114">-Profile</span></span>
<span data-ttu-id="3e44c-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e44c-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e44c-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3e44c-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e44c-117">-TrackingId</span><span class="sxs-lookup"><span data-stu-id="3e44c-117">-TrackingId</span></span>
<span data-ttu-id="3e44c-118">Określa identyfikator śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3e44c-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e44c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e44c-119">CommonParameters</span></span>
<span data-ttu-id="3e44c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e44c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e44c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e44c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e44c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e44c-122">INPUTS</span></span>

## <span data-ttu-id="3e44c-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e44c-123">OUTPUTS</span></span>

## <span data-ttu-id="3e44c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e44c-124">NOTES</span></span>

## <span data-ttu-id="3e44c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e44c-125">RELATED LINKS</span></span>

[<span data-ttu-id="3e44c-126">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="3e44c-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="3e44c-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e44c-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="3e44c-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3e44c-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


