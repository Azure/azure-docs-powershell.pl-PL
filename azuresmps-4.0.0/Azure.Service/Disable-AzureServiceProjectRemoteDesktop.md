---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054662"
---
# <span data-ttu-id="02223-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="02223-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="02223-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02223-102">SYNOPSIS</span></span>
<span data-ttu-id="02223-103">Wyłącza dostęp pulpitu zdalnego do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="02223-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="02223-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02223-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02223-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02223-105">DESCRIPTION</span></span>
<span data-ttu-id="02223-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="02223-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02223-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="02223-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="02223-108">**Element Disable-AzureServiceProjectRemoteDesktop** wyłącza dostęp pulpitu zdalnego do usługi hostowanej.</span><span class="sxs-lookup"><span data-stu-id="02223-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="02223-109">Aby zmiany zostały wprowadzone, należy opublikować usługę za pomocą polecenia cmdlet **Publish-AzureServiceProject** po wyłączeniu dostępu do pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="02223-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="02223-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02223-110">EXAMPLES</span></span>

## <span data-ttu-id="02223-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02223-111">PARAMETERS</span></span>

### <span data-ttu-id="02223-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02223-112">-PassThru</span></span>
<span data-ttu-id="02223-113">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="02223-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02223-114">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="02223-114">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02223-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="02223-115">-Profile</span></span>
<span data-ttu-id="02223-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02223-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02223-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="02223-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02223-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02223-118">CommonParameters</span></span>
<span data-ttu-id="02223-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02223-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02223-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02223-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02223-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02223-121">INPUTS</span></span>

## <span data-ttu-id="02223-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02223-122">OUTPUTS</span></span>

## <span data-ttu-id="02223-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02223-123">NOTES</span></span>

## <span data-ttu-id="02223-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02223-124">RELATED LINKS</span></span>

[<span data-ttu-id="02223-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="02223-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


