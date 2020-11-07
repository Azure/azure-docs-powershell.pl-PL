---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 1c89db6267fffeb73820150d1c73c3225f45cde2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527729"
---
# <span data-ttu-id="b3e20-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="b3e20-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="b3e20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3e20-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e20-103">Powoduje ponowne zarejestrowanie serwera w celu nawiązania połączenia z magazynem kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="b3e20-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3e20-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3e20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b3e20-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e20-106">Polecenie cmdlet **enable-AzureRmBackupContainerReregistration** umożliwia ponowne zarejestrowanie serwera w celu nawiązania połączenia z magazynem kopii zapasowych platformy Azure i kontynuowanie łańcucha punktów odzyskiwania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="b3e20-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>

<span data-ttu-id="b3e20-107">W przypadku zniszczenia serwera wszystkie punkty kopii zapasowej w chmurze pozostaną w magazynie kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="b3e20-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="b3e20-108">Jeśli utworzysz serwer zastępczy i przypiszesz mu tę samą w pełni kwalifikowaną nazwę domeny, możesz połączyć serwer z powrotem do tego samego magazynu.</span><span class="sxs-lookup"><span data-stu-id="b3e20-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="b3e20-109">To polecenie cmdlet umożliwia wykonywanie kopii zapasowych i dodawanie nowych punktów kopii zapasowej do istniejącego zestawu.</span><span class="sxs-lookup"><span data-stu-id="b3e20-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="b3e20-110">Nowy serwer nadal znajduje się w łańcuchu kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="b3e20-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="b3e20-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3e20-111">EXAMPLES</span></span>

## <span data-ttu-id="b3e20-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3e20-112">PARAMETERS</span></span>

### <span data-ttu-id="b3e20-113">-Kontener</span><span class="sxs-lookup"><span data-stu-id="b3e20-113">-Container</span></span>
<span data-ttu-id="b3e20-114">Określa kontener, który zostanie ponownie przerejestrowany przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="b3e20-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="b3e20-115">Aby uzyskać **AzureRmBackupContainer** , użyj polecenia cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="b3e20-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e20-116">-DefaultProfile</span></span>
<span data-ttu-id="b3e20-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3e20-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3e20-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e20-118">CommonParameters</span></span>
<span data-ttu-id="b3e20-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e20-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e20-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e20-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e20-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3e20-121">INPUTS</span></span>

### <span data-ttu-id="b3e20-122">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b3e20-122">AzureBackupContainer</span></span>

## <span data-ttu-id="b3e20-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3e20-123">OUTPUTS</span></span>

### <span data-ttu-id="b3e20-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b3e20-124">None</span></span>

## <span data-ttu-id="b3e20-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3e20-125">NOTES</span></span>

## <span data-ttu-id="b3e20-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3e20-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3e20-127">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b3e20-127">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b3e20-128">Rejestr — AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b3e20-128">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

