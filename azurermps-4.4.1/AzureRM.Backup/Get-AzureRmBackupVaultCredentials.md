---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: b208602532428d14c2af1504c5b8af2cce0b155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528285"
---
# <span data-ttu-id="79edc-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="79edc-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="79edc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79edc-102">SYNOPSIS</span></span>
<span data-ttu-id="79edc-103">Pobiera plik poświadczeń magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="79edc-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79edc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79edc-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79edc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79edc-105">DESCRIPTION</span></span>
<span data-ttu-id="79edc-106">Polecenie cmdlet **Get-AzureRmBackupVaultCredentials** pobiera plik poświadczeń magazynu dla magazynu kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79edc-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="79edc-107">Funkcja kopii zapasowej używa pliku poświadczeń magazynu, aby połączyć serwer z magazynem kopii zapasowych platformy Azure i zarejestrować go.</span><span class="sxs-lookup"><span data-stu-id="79edc-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="79edc-108">Zanim kopia zapasowa będzie mogła wysłać kopię zapasową do magazynu, musisz zarejestrować serwer.</span><span class="sxs-lookup"><span data-stu-id="79edc-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="79edc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79edc-109">EXAMPLES</span></span>

## <span data-ttu-id="79edc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79edc-110">PARAMETERS</span></span>

### <span data-ttu-id="79edc-111">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="79edc-111">-TargetLocation</span></span>
<span data-ttu-id="79edc-112">Określa ścieżkę docelową, w której to polecenie cmdlet przechowuje plik poświadczeń magazynu.</span><span class="sxs-lookup"><span data-stu-id="79edc-112">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79edc-113">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="79edc-113">-Vault</span></span>
<span data-ttu-id="79edc-114">Określa magazyn kopii zapasowych, dla którego to polecenie cmdlet pobiera plik poświadczeń magazynu.</span><span class="sxs-lookup"><span data-stu-id="79edc-114">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="79edc-115">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="79edc-115">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79edc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79edc-116">-DefaultProfile</span></span>
<span data-ttu-id="79edc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79edc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79edc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79edc-118">CommonParameters</span></span>
<span data-ttu-id="79edc-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79edc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79edc-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79edc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79edc-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79edc-121">INPUTS</span></span>

### <span data-ttu-id="79edc-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="79edc-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="79edc-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79edc-123">OUTPUTS</span></span>

### <span data-ttu-id="79edc-124">Ciąg</span><span class="sxs-lookup"><span data-stu-id="79edc-124">String</span></span>
<span data-ttu-id="79edc-125">To polecenie cmdlet zwraca nazwę pliku poświadczeń magazynu.</span><span class="sxs-lookup"><span data-stu-id="79edc-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="79edc-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79edc-126">NOTES</span></span>

## <span data-ttu-id="79edc-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79edc-127">RELATED LINKS</span></span>

[<span data-ttu-id="79edc-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="79edc-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


