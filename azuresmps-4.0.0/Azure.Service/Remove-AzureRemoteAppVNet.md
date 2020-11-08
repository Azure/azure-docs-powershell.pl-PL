---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055112"
---
# <span data-ttu-id="9c3d0-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="9c3d0-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="9c3d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3d0-103">Usuwa sieć wirtualną funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="9c3d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c3d0-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c3d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c3d0-105">DESCRIPTION</span></span>
<span data-ttu-id="9c3d0-106">Polecenie cmdlet **Remove-AzureRemoteAppVNet** usuwa sieć wirtualną funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="9c3d0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c3d0-107">EXAMPLES</span></span>

### <span data-ttu-id="9c3d0-108">Przykład 1: usunięcie określonej sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9c3d0-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="9c3d0-109">To polecenie usuwa sieć wirtualną o nazwie ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="9c3d0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c3d0-110">PARAMETERS</span></span>

### <span data-ttu-id="9c3d0-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="9c3d0-111">-Profile</span></span>
<span data-ttu-id="9c3d0-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c3d0-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c3d0-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9c3d0-114">-VNetName</span></span>
<span data-ttu-id="9c3d0-115">Określa nazwę sieci wirtualnej usługi Azure RemoteApp, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3d0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3d0-116">CommonParameters</span></span>
<span data-ttu-id="9c3d0-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3d0-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c3d0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3d0-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c3d0-119">INPUTS</span></span>

## <span data-ttu-id="9c3d0-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c3d0-120">OUTPUTS</span></span>

## <span data-ttu-id="9c3d0-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c3d0-121">NOTES</span></span>

## <span data-ttu-id="9c3d0-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c3d0-122">RELATED LINKS</span></span>

[<span data-ttu-id="9c3d0-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="9c3d0-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="9c3d0-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="9c3d0-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


